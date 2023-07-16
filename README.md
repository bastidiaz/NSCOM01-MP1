# Simple TFTP Client
#### Class requirement for NSCOM01 in De La Salle University
* Support for both upload and download of binary files
* When uploading:
  * The program can send any file on the computer to the TFTP server as long as the file is accessible to the user using his / her OS privileges
* When downloading:
  * The program must allow the user to provide the filename to use when saving the downloaded file to the client computer
* Proper error handling which at the minimum should include the following:
  * Timeout for unresponsive server
  * Handling of duplicate ACK
  * User prompt for file not found, access violation, and disk full errors
