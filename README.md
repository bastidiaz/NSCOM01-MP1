# Simple TFTP Client (CLI)
#### Features
* Support for both upload and download of binary files
* When uploading:
  * The program can send any file on the computer to the TFTP server as long as the file is accessible to the user using his / her OS privileges
* When downloading:
  * The program must allow the user to provide the filename to use when saving the downloaded file to the client computer
* Proper error handling which at the minimum should include the following:
  * Timeout for unresponsive server
  * Handling of duplicate ACK
  * User prompt for file not found, access violation, and disk full errors

### How to use
* Start a TFTP server (client was tested using [TFTPD64](https://pjo2.github.io/tftpd64/)) TFTP server)
* Run the program on the command line/terminal: `python client.py`
* You will be prompted for a server IP address (enter the address of your TFTP server running on port `69`)
* You will be asked to select a mode of transfer: `netascii` or `octet` (read more [here](https://www.ibm.com/docs/en/zvm/7.2?topic=subcommands-mode))
* You will be prompted for an action: `upload`, `download`, or `exit`
  * `upload` will ask for the name of the file to be uploaded (include its path, if necessary; `files/FileA.jpg`, for example) and then the name that shall be reflected in the server (or its path, if necessary, as mentioned before); you cannot create new folders through the client and will throw an exception
  * `download` will ask for the name of the file to be downloaded as it exists the server  (include its path, if necessary) and then the name that it will be saved us on the client (or its path); you cannot create new folders through the client and will throw an exception
  * `exit` quits the program in its entirety
