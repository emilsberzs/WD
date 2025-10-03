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

- Querying the screen size:
    - Window (viewport) size
    - Screen size
    - Available screen size
    - Document size
```
<script>
    document.write("Window (viewport) size: " + window.innerWidth + "x" + 
                    window.innerHeight)
    document.write("Screen size: " + screen.width + "x" + screen.height)
    document.write("Available screen size: " + screen.availWidth + "x" + 
                    screen.availHeight)
    document.write("Document size:" + document.documentElement.clientWidth + "x"+       document.documentElement.clientHeight)
</script>
```

- Also have take into accout CPU capability of different devices
- Consider input devices (stilus, VR, voice?)
- And dont forget that internet is not reliable.

### Server access logs
- Content:
    - IP address
    - Timestamp
    - Request type
    - Request target
    - HTTP version
    - Response code
    - User agent string

- Importance of analysing server access logs:
    - Security monitoring eg. checking sketchy IP's repeatedly querying 
    - Performance monitoring
    - Troubleshooting
    - Revealing patterns eg. usage patterns.

- Command line tools for analysing server access logs:  
    - tail: simple tool to follow server logs
        ```
        >>>tail -f /path/to/log/access/log
        ```
    - go access: parses the logfile and formats into dashboard for easier viewing
        ```
        goaccess logfiles.log -o report.html --log-format=COMBINED
        ```