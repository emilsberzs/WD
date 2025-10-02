## Layout for different devices: Who and why accesses websites?

### Ecosystem of the internet: clients, servers, humans and machines
- What is a client:
    - Anything that issues requests:
        - Browsers
        - Web applications
        - Wep spiders (crawlers)
- Who are You?
    - The User agent string, introduced in 1993:
        ```
        <field>    =User-Agent: <product>+
        <product>  =<word> [/<version>]
        <version>  =<word>
        ```
- Detecting user agents:
    - Server-side (via HTTP header)
    - Client-side (Javascript)
- Top web servers: 
    - Nginx
    - Apache
    - Cloudflare
### Security threats in the microsystem
- Phishing: the server pretends to be something it is not (fake sites)
- DDOS(distributed-denial-of-service): many clients (botnet) work together to overload server
- Man-in-th-middle: given the complexity of data flows, can sit in the middle and capture data (intercepting data, HTTPS should solve it, no?)

### Hardware used to access th internet
- All the usual suspects with different screen sizes and interaction types that have to be taken into account when designing web sites (including accessibility features)

