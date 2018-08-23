Review：
What is networking protocols:
It is the standard of how server and computers communicate.

Transport Layer protocol:
TCP and UDP:
major difference: TCP is a connection oriented protocol, but UDP is a connectionless oriented protocol.

UDP includes the information of source port and destination port, length(header and data), checksum(optional, used to check if the message is correct or not).

More information: https://www.coursera.org/lecture/internet-technologies/udp-protocol-nqXQb

What is the port of a computer: port number is an unique ID of the protocol in the computer networking. It is used to
differentiate server and client simply or represent certain type of protocol.

![alt text](https://github.com/getstart1/blogs-notes/blob/master/images/1.png)

The image comes from the youTube video at the following:
https://www.youtube.com/watch?v=xqJj0kT95LA


How to check the port number of your own computer:
Terminal: netstat -a

In what situations do we use TCP or UDP:

  UDP: Anything where you don't care too much if you get all data always

    Tunneling/VPN (lost packets are ok - the tunneled protocol takes care of it)
    Media streaming (lost frames are ok)
    Games that don't care if you get every update
    Local broadcast mechanisms (same application running on different machines "discovering" each other)


  TCP: Almost anything where you have to get all transmitted dataWeb
    SSH, FTP, telnet
    SMTP, sending mail
    IMAP/POP, receiving mail


7 layers of OSI model:
link: https://www.webopedia.com/quick_ref/OSI_Layers.asp

Application Level Protocols
A high level protocol in OSI model, it targets at the application, and ignore details for other lower level protocols at the same time. 
One example is HTTP:
1) Client and Server model: client request and server response. 
2) HTTP headers allow clients and servers to include additional information
resource: https://www.youtube.com/watch?v=k6fy7mvNSnY

Another example is HTTPS:
HTTPS encrypt the sensitive data so it is a safer application protocol than HTTP. 
https://www.youtube.com/watch?v=0PHCAdw6Z8w

IRC(Internet Relay Chat):
This is an application protocol that facilitates communication in the form of text. 
Try http://webchat.freenode.net/    One example of Internet Relay Chat
 
This is the example of various commands of IRC: 
https://en.wikipedia.org/wiki/List_of_Internet_Relay_Chat_commands

FTP(File Transfer Protocol): Application level protocol used for the transfers of computer files between a client and server on a computer network. 








