I learned how to split the words in a string sentence by using s.split(" ")
The problem I have encountered is that I missed the space in quotation marks(""), so the characters are splited.

The coding questions I worked on today is to find the shortest word in a string.
My code is as the following:
```
function findShort(s){
  var words = s.split(" ");
  var shortest = 1000;
  var len = 0;
  for (var i = 0; i< words.length; i++){
    len = words[i].length;
    if (len < shortest){
      shortest = len;
    }
  }
  return shortest;
}
```


Next step: I want to study for the materials that I am going to teach tomorrow.
Topics: Networking protocols


Prepare for tutoring tomorrow. I found out that when I know that I can export my knowledge, I would feel more motivated when import my knowledge.

The topic: Networking protocols

Network protocol is a set of rules that computers and servers communicate with each other. It exists because both the computer and server need to follow the same communication rule in order to function well. What are the materials that need to communicate: files that server send to computers, input that computers need to send to servers.
resource: https://www.youtube.com/watch?v=BfZ0zZGT0_k

Comparing TCP and UDP:
TCP: Transmission control protocol
UDP: User datagram protocol
The major difference is that UDP is a connectionless oriented protocol whereas TCP is a connection oriented protocol. TCP takes more time because it is a three way communication. UDP is a one way sending information, and the sender does not care if the receiver receives them or not.

Question: In what kind of situation do we use TCP and UDP?

resource: https://www.youtube.com/watch?v=uwoD5YsGACg
