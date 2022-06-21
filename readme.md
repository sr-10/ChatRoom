# ChatRoom
![logo](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)

## Description
Chatroom is a C++ based project for enabling multiple users to have conversation at a common place.

## Concepts Used In Project
- Threads
    - To handle each client separately by server.
    - To send and recieve messages  by client.
- Mutex
    - To add each client to the client list avoiding the problem of process synchronisation.
    - To send the messages in order which is ensuring a message is delivered to all users before sending another one.
- Socket Programming
    - To create client-server model.
## Dependencies:
   - Text Editor
   - C++ Compiler
   - WSL/Linux/Mac
## Installation
- Clone the repository.
- Open the repository from the terminal.
- Type in terminal the command: g++ -pthread -o server_chat server_chat.cpp
- Type in terminal the command: ./server_chat 3434(This is the port number. You can type any other of your own wish also.)
- Open another terminal and go to the same directory where project is located.
- Type in terminal the command:g++ -pthread -o client_chat client_chat.cpp
- Type in terminal the command: ./client_chat 3434(This number needs to be same as the server one.)
- Enter your name and you are ready to go.
- You can connect multiple clients by opening the project from multiple terminal and writing the command ./client_chat 3434.
## 

## Features
- Multiple clients can chat at a common place.
- Every user gets to see who is the sender of each message.
- No messages are lost and using mutex the order of message delivery is taken care.
- All the users can see when a new user joins the room or leaves it.

## Working of the Project
The ChatRoom Project is client-server model where the server is multithreaded, so that it can support multiple clients at same time. Using threads we handle the multiple client that are requesting to join our chat room. The use of mutex is necessary where multiple clients wants to join the room at same time, we need to use mutex in order to add the clients one by one. This helps in avoiding the problem of process synchronisation. The client also uses separate threads for sending and recieving messages as both of the processes may occur concurrently. The client sends the message to the server and then the server forwards it to all the other clients in the chatroom. Mutex are again used here where we ensure that a message is sent to every client before sending another one.

## Learnings from the Project
- Socket Programming
- Use of multithreading
- Use of mutex in server
## Links
To understand the concepts used in more detail, you can refer to following links.
- [Socket Programming](https://www.geeksforgeeks.org/socket-programming-cc/)
- [Pthreads](https://www.geeksforgeeks.org/thread-functions-in-c-c/)
- [Multithreading](https://www.geeksforgeeks.org/multithreading-in-cpp/)
- [Mutex](https://www.geeksforgeeks.org/mutex-lock-for-linux-thread-synchronization/)
