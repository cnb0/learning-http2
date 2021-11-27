1. Moving to HTTP/2

Chapter 1. Web technologies and HTTP

            1.1. How the web works
                1.1.1. The internet versus the World Wide Web
                1.1.2. What happens when you browse the web?
            1.2. What is HTTP?
            1.3. The syntax and history of HTTP
                1.3.1. HTTP/0.9
                1.3.2. HTTP/1.0
                1.3.3. HTTP/1.1
            1.4. Introduction to HTTPS
            1.5. Tools for viewing, sending, and receiving HTTP messages
                1.5.1. Using developer tools in web browsers
                1.5.2. Sending HTTP requests
                1.5.3. Other tools for viewing and sending HTTP requests

  

Chapter 2. The road to HTTP/2

            2.1. HTTP/1.1 and the current World Wide Web
                2.1.1. HTTP/1.1’s fundamental performance problem
                2.1.2. Pipelining for HTTP/1.1
                2.1.3. Waterfall diagrams for web performance measurement
            2.2. Workarounds for HTTP/1.1 performance issues
                2.2.1. Use multiple HTTP connections
                2.2.2. Make fewer requests
                2.2.3. HTTP/1 performance optimizations   
            2.3. Other issues with HTTP/1.1
            2.4. Real-world examples
                2.4.1. Example website 1: amazon.com
                2.4.2. Example website 2: imgur.com
                2.4.3. How much of a problem is this really?
            2.5. Moving from HTTP/1.1 to HTTP/2
                2.5.1. SPDY
                2.5.2. HTTP/2
            2.6. What HTTP/2 means for web performance
                2.6.1. Extreme example of the power of HTTP/2
                2.6.2. Setting expectations of HTTP/2 performance gains
                2.6.3. Performance workarounds for HTTP/1.1 as potential antipatterns

  

Chapter 3. Upgrading to HTTP/2

            3.1. HTTP/2 support
                3.1.1. HTTP/2 support on the browser side
                3.1.2. HTTP/2 support for servers
                3.1.3. Fallback when HTTP/2 isn’t supported
            3.2. Ways to enable HTTP/2 for your website
                3.2.1. HTTP/2 on your web server
                3.2.2. HTTP/2 with a reverse proxy
                3.2.3. HTTP/2 through a CDN
                3.2.4. Implementing HTTP/2   
            3.3. Troubleshooting HTTP/2 setup

  

2. Using HTTP/2

Chapter 4. HTTP/2 protocol basics

            4.1. Why HTTP/2 instead of HTTP/1.2?
                4.1.1. Binary rather than textual
                4.1.2. Multiplexed rather than synchronous
                4.1.3. Stream prioritization and flow control
                4.1.4. Header compression
                4.1.5. Server push
            4.2. How an HTTP/2 connection is established
                4.2.1. Using HTTPS negotiation
                4.2.2. Using the HTTP upgrade header
                4.2.3. Using prior knowledge
                4.2.4. HTTP Alternative Services
                4.2.5. The HTTP/2 preface message
            4.3. HTTP/2 frames
                4.3.1. Viewing HTTP/2 frames
                4.3.2. HTTP/2 frame format
                4.3.3. Examining HTTP/2 message flow by example
                4.3.4. Other frames


Chapter 5. Implementing HTTP/2 push

            5.1. What is HTTP/2 server push?
            5.2. How to push
                5.2.1. Using HTTP link headers to push
                5.2.2. Viewing HTTP/2 pushes
                5.2.3. Pushing from downstream systems by using link headers
                5.2.4. Pushing earlier
                5.2.5. Pushing in other ways
            5.3. How HTTP/2 push works in the browser
                5.3.1. Seeing how the push cache works
                5.3.2. Refusing pushes with RST_STREAM
            5.4. How to push conditionally
                5.4.1. Tracking pushes on the server side
                5.4.2. Using HTTP conditional requests
                5.4.3. Using cookie-based pushes
                5.4.4. Using cache digests
            5.5. What to push
                5.5.1. What can you push?
                5.5.2. What should you push?
                5.5.3. Automating push
            5.6. Troubleshooting HTTP/2 push
            5.7. The performance impact of HTTP/2 push
            5.8. Push versus preload
            5.9. Other use cases for HTTP/2 push

  

Chapter 6. Optimizing for HTTP/2

            6.1. What HTTP/2 means for web developers
            6.2. Are some HTTP/1.1 optimizations now antipatterns?
                6.2.1. HTTP/2 requests still have a cost
                6.2.2. HTTP/2 isn’t limitless
                6.2.3. Compression is more efficient for larger resources
                6.2.4. Bandwidth limitations and resource contention
                6.2.5. Sharding
                6.2.6. Inlining
                6.2.7. Conclusion
            6.3. Web performance techniques still relevant under HTTP/2
                6.3.1. Minimizing the amount of data transferred
                6.3.2. Using caching to prevent resending data
                6.3.3. Service workers can further reduce load on the network
                6.3.4. Don’t send what you don’t need
                6.3.5. HTTP resource hints
                6.3.6. Reduce last-mile latency
                6.3.7. Optimize HTTPS
                6.3.8. Non-HTTP-related web performance techniques
            6.4. Optimizing for both HTTP/1.1 and HTTP/2
                6.4.1. Measuring HTTP/2 traffic
                6.4.2. Detecting HTTP/2 support on the server side
                6.4.3. Detecting HTTP/2 support on the client side
                6.4.4. Connection coalescing
                6.4.5. How long to optimize for HTTP/1.1 users

  

3. Advanced HTTP/2

Chapter 7. Advanced HTTP/2 concepts

            7.1. Stream states
            7.2. Flow control
                7.2.1. Example of flow control
                7.2.2. Setting flow control on the server
            7.3. Stream priorities
                7.3.1. Stream dependencies
                7.3.2. Stream weighting
                7.3.3. Why does prioritization need to be so complicated?
                7.3.4. Prioritization in web servers and browsers
            7.4. HTTP/2 conformance testing
                7.4.1. Server conformance testing
                7.4.2. Client conformance testing

  

Chapter 8. HPACK header compression

            8.1. Why is header compression needed?
            8.2. How compression works
                8.2.1. Lookup tables
                8.2.2. More-efficient encoding techniques
                8.2.3. Lookback compression
            8.3. HTTP body compression
            8.4. HPACK header compression for HTTP/2
                8.4.1. HPACK static table
                8.4.2. HPACK dynamic table
                8.4.3. HPACK header types
                8.4.4. Huffman encoding table
                8.4.5. Huffman encoding script
                8.4.6. Why Huffman encoding isn’t always optimal
            8.5. Real-world examples of HPACK compression
            8.6. HPACK in client and server implementations
            8.7. The value of HPACK

  

4. The future of HTTP

Chapter 9. TCP, QUIC, and HTTP/3

            9.1. TCP inefficiencies and HTTP
                9.1.1. Setup delay in creating an HTTP connection
                9.1.2. Congestion control inefficiencies in TCP
                9.1.3. Effect of TCP inefficiencies on HTTP/2
                9.1.4. Optimizing TCP
                9.1.5. The future of TCP and HTTP
            9.2. QUIC
                9.2.1. Performance benefits of QUIC
                9.2.2. QUIC and the internet stack
                9.2.3. What UDP is and why QUIC is built on it
                9.2.4. Standardizing QUIC
                9.2.5. Differences between HTTP/2 and QUIC
                9.2.6. QUIC tools
                9.2.7. QUIC implementations
                9.2.8. Should you use QUIC?

  

Chapter 10. Where HTTP goes from here

            10.1. Controversies of HTTP/2 and what it didn’t fix
                10.1.1. Arguments against SPDY
                10.1.2. Privacy issues and state in HTTP
                10.1.3. HTTP and encryption
                10.1.4. Transport protocol issues
                10.1.5. HTTP/2 is far too complicated
                10.1.6. HTTP/2 is a stopgap
            10.2. HTTP/2 in the real world
            10.3. Future versions of HTTP/2 and what HTTP/3 or HTTP/4 may bring
                10.3.1. Is QUIC HTTP/3?
                10.3.2. Evolving the HTTP binary protocol further
                10.3.3. Evolving HTTP above the transport layer
                10.3.4. What would require a new HTTP version?
                10.3.5. How future versions of HTTP might be introduced
                10.4. HTTP as a more generic transport protocol
                10.4.1. Using HTTP semantics and messages to deliver nonweb traffic
                10.4.2. Using the HTTP/2 binary framing layer
                10.4.3. Using HTTP to start another protocol

  

Appendix. Upgrading common web servers to HTTP/2

            A.1. Upgrading your web server to support HTTP/2
            A.1.1. Apache
            A.1.2. nginx
            A.1.3. Microsoft Internet Information Services (IIS)
            A.1.4. Other servers
            A.2. Setting up HTTP/2 via a reverse proxy server
            A.2.1. Apache
            A.2.2. nginx