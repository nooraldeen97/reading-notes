## High-level HTTP<br>

#### Step 1: Local Processing: <br>

- If the cache lookup fails, your browser fires off a DNS request using UDP3. The DNS request contains the <br>preconfigured IP for your DNS server and your return IP in its header.<br>
- Your request will now have to travel many network devices to reach its target DNS server.<br>
- Once your request arrives at your configured DNS server, the server looks for the address associated with the <br>requested hostname. If it finds one, it sends a response. If, on the other hand, the DNS server you have <br>targeted cannot locate the given hostname, it passes the request along to another DNS server it is <br>configured to defer to. This happens recursively until the address is found, or an "authoritative" <br>nameserver is hit.<br>
- If the response makes it back (remember, with UDP there’s no guarantee!), the requesting client now has a <br>target IP. It will also have received a piece of information as part of the answer that will let it know<br> how long the returned answer can be cached for.<br>


#### Step 3: Establish a TCP Connection:<br>

- One of the key differences between TCP and UDP is that TCP ensures delivery and ordered data transmission.<br>
- TCP connections are opened using what’s known as a three-way handshake. The server must already be <br>"listening" on a port, performing a passive open, after which the client can initiate an active open.<br>
- full duplex communication: bidirectional, concurrent communication along the connection<br>

#### Step 4: Send an HTTP Request: <br>

- The request is made up of a "request line", request header, and a body.<br>
Two consecutive pairs indicate the end of the header section<br>
The only mandatory field in an HTTP request is HOST, which contains the domain and port that the request is<br> being sent to (domain.com:8080), although in some cases the port can be omitted.<br>
common standard HTTP header fields include Origin, Accept, Accept-Encoding<br>
- Once the HTTP request is sent using TCPs magic sequence number powers, the server can ensure it receives the <br>whole request, in the correct order.<br>
- Once the server receives the request, processes it, and finds the resource being requested, it generates an <br>HTTP response.<br>
- Once the response is generated, the server responds to the request. At the TCP layer, the client receives the<br> first data packet, the first byte of which should contain the HTTP response header.<br>


#### Step 5: Tearing Down and Cleaning Up:<br>

- Once the response has been fully delivered, the client sends a FIN packet at the TCP level, to which the<br> server responds with an ACK, and then generally sends a FIN of its own, which the client responds to with its <br>own ACK signal.<br>
- The client then waits for a brief timeout, during which it cannot accept new connections, to prevent delayed<br> packets from previous connections arriving during subsequent activities on the port. This four way<br> handshake12 signals the end of the TCP connection.<br>
- At this point, your browser begins processing what it has received.<br>


## Java HTTP Request example<br>

#### HttpUrlConnection<br>

- The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional <br>libraries<br>
- The disadvantages of using this method are that the code can be more cumbersome than other HTTP libraries and<br> that it does not provide more advanced functionalities such as dedicated methods for adding headers or <br>authentication.<br>

#### Creating a Request<br>

- We can create an HttpUrlConnection instance using the openConnection() method of the URL class.<br>
- The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one <br>of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.<br>


1- Adding Request Parameters<br>
2- Setting Request Headers<br>


#### Reading the Response<br>
- Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.<br>

- To execute the request, we can use the `getResponseCode()`, `connect()`,` getInputStream()` or <br>`getOutputStream`() methods.


