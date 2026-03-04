# Lesson 071: Async I/O Part B: Async Networking

## Section 14: Async Rust

## Status: pending

## Added
- Split from original lesson 070 (v7 pacing review)

## Objectives
- [ ] Build an async TCP server using `tokio::net::TcpListener` and `TcpStream`, accepting multiple connections concurrently
- [ ] Use `tokio::spawn` to handle each connection in its own task, reading and writing lines with `tokio::io::BufReader` and `AsyncBufReadExt`/`AsyncWriteExt`
- [ ] Understand why async networking is more efficient than spawning a thread per connection (event-driven, non-blocking, OS epoll/kqueue under the hood)
- [ ] Extend a basic echo server toward a real protocol (line-based framing, graceful shutdown, or multi-client interaction)

## Exercises
- [ ] **Echo TCP server**: Build an async TCP echo server that binds to a port, accepts multiple connections concurrently using a loop over `listener.accept()`, and spawns a task per connection that reads lines (using `BufReader`) and echoes them back. Test with `telnet localhost <port>` or a simple async client you write

> **Build it step by step:**
> 1. `TcpListener::bind("127.0.0.1:8080").await?` — bind the listener
> 2. Loop with `listener.accept().await?` — accept connections
> 3. For each connection, `tokio::spawn` a task to handle it
> 4. Inside the task: wrap the stream in `BufReader::new(stream)`
> 5. Use `reader.read_line(&mut buf).await?` in a loop to read lines
> 6. Write each line back with `writer.write_all(buf.as_bytes()).await?`
> 7. Test with: `telnet 127.0.0.1 8080` or `nc localhost 8080`
- [ ] **Multi-client chat or protocol extension** (pick one):
  - *Option A - Chat server*: Extend the echo server so that messages from any client are broadcast to all connected clients using `tokio::sync::broadcast` channel
  - *Option B - Line-based protocol*: Extend the echo server to support simple commands: `UPPER <text>` echoes back uppercased, `REVERSE <text>` echoes back reversed, `QUIT` closes the connection gracefully

## Notes
_Lesson not yet started._
