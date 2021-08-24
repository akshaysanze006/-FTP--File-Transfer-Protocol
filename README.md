# -FTP--File-Transfer-Protocol

FTP is a protocol for transfering files between local hosts and remote hosts. The user at thelocal  host provides the host name of the remote host to the FTP client process on the local host.This  creates a connection between local host client process and remote host server process. Theuser  then provides identification and password to the server which authorizes the user. Now filescan be  transferred between hosts. FTP uses two parallel connections to transfer a file.One connection is  called control connection and other connection is called the data connection.The commands get  and put are sent over FTP control connection. The data connection isused for sending the files.  When the user starts FTP session, the client establishes the controlconnection with the remote  server. When the server gets a command to transfer a file, the serverestablishes a data connection.  After the file transfer, the data connection is closed. To sendanother file, a new data connection is  established. So control connection is persistent during entire FTP session. However the data  connection breaks after each data transfer. When a localmachine is connected with remote server  through FTP, it will receive a terminal of server. Thenthe communcation is based on set of FTP  comands. The following are a sublist of popular FTPcommands. 


Algorithm:  
• Client Connection 
1. Read input from user 
2. If input==’1’. 
3. call receivefile() 
4. Else 
5. If input==’2’ 
6. call sendfile(filename) 
7. Search file name. 
8. If exists, convert it into bytes. 
9. send to output stream. 
10. sendfile() 
11. open the file with filename. 
12. convert into byte array 
13. Else 
14. Error

• File Server 
1.Create server socket. 
2. Listen for client. 
3. If new client received, create a new thread. 
4. Start the thread. 
• File Client 
1. Create client socket. 
2. Read integer from the console 
3. If input ==’1’ 
4. sendfile() 
5. If input == ‘2’ 
6. readfilename() 
7.receive file. 
