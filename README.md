# Java Socket-Based Web Server

Three versions of a TCP socket server in Java, showing how a server handles concurrent clients.

- **SingleThreaded**: handles one client at a time. The server times out after 20 seconds with no incoming connection.
- **MultiThreaded**: creates a new thread for each client connection.
- **ThreadPool**: reuses a fixed pool of 10 worker threads via `ExecutorService`, avoiding the cost of creating a thread for every client.

The MultiThreaded client simulates 100 concurrent connections to load-test the server.

## Run
1. Compile: `javac *.java` inside a folder
2. Start the server: `java Server`
3. In another terminal, run the client: `java Client`
