# Lesson 100: Networking - reqwest, hyper, raw TCP/UDP

## Section 19: Ecosystem & Tooling

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Make HTTP GET and POST requests using `reqwest` (async as the primary path), parsing JSON responses with serde
- [ ] Understand `hyper` as the lower-level HTTP library that `reqwest` builds on, and when you would use each (compare with Go's `net/http` which sits between the two in abstraction level)
- [ ] Build a raw TCP client and server using `std::net::TcpListener` and `TcpStream`, handling connections with threads
- [ ] Configure HTTP clients with custom headers, timeouts, and connection pooling using `reqwest::Client` builder
- [ ] [OPTIONAL] Send and receive UDP datagrams using `std::net::UdpSocket`, understanding when UDP is appropriate vs TCP

## Exercises
- [ ] **Exercise 1 - REST API Client**: Use `reqwest` async client to fetch data from a public REST API (e.g., `httpbin.org` or `jsonplaceholder.typicode.com`), deserialize the JSON response into a struct, and print formatted output. After that works, optionally add a blocking-client version and compare ergonomics.
- [ ] **Exercise 2 - TCP Echo Server**: Build a TCP echo server that accepts multiple concurrent connections using `std::net::TcpListener` with `thread::spawn`, where the server reads a line from the client and sends it back uppercased; write a companion TCP client that connects, sends a message, and prints the response

  > **Server skeleton:**
  > ```rust
  > use std::net::{TcpListener, TcpStream};
  > use std::io::{BufRead, BufReader, Write};
  > use std::thread;
  >
  > fn handle_client(stream: TcpStream) {
  >     let reader = BufReader::new(&stream);
  >     let mut writer = stream.try_clone().expect("clone failed");
  >     for line in reader.lines() {
  >         let line = line.expect("read failed");
  >         writeln!(writer, "{}", line.to_uppercase()).expect("write failed");
  >     }
  > }
  >
  > fn main() {
  >     let listener = TcpListener::bind("127.0.0.1:7878").expect("bind failed");
  >     for stream in listener.incoming() {
  >         let stream = stream.expect("accept failed");
  >         thread::spawn(|| handle_client(stream));
  >     }
  > }
  > ```
- [ ] **Exercise 3 - UDP Datagrams [STRETCH]**: Write a UDP program with two modes: a sender that sends timestamped messages to a target address, and a receiver that listens and prints incoming datagrams -- demonstrate that messages can arrive out of order or be lost
- [ ] **Exercise 4 [STRETCH] - HTTP client with retries and configuration**: Build an HTTP client function using `reqwest::Client` that sets a custom `User-Agent` header, a 5-second timeout, and retries a request up to 3 times on failure, then use it to fetch from a URL passed as a command-line argument

## Notes
> **Internet required**: Exercise 1 requires internet access to reach a public API (e.g., `httpbin.org` or `jsonplaceholder.typicode.com`). Ensure you have a working connection before starting.
> **Scope recommendation**: Core path is Exercises 1-2 (~60-90 min). Pick at most one stretch exercise (3 or 4) in the same session.

_Lesson not yet started._
