# 1. The internet and HTTP
  
## History of internet 
- Conceptual foundations early 60s
- ARPANET 60s-70s
- Standartization and expansion 70s
- Commercialisation and expansion 80s-90s
   
### ARPANET (1960s-1970s)
- 1957 DARPA (Defense Advanced Research Projects Agency)
- Circuit switching was tried first but didnt work, as wouldnt scale.
- 1967 packet switching by Leonard Kleinrock, chopping data into packets and sending over the network, no need for permanent connection and other benefits
- 1968 First interface message processor, Router.

### Expansion and Standartisation (1970s)
 - 1972 Bob KAHN demonstrates 20 node demo at ICCC ( International Computer Communication Conference). Later he worked on TCP/IP
 - 1972 Ray Tomlinson at BBN wrote first email software
 - 1973 Peter Kirstein and team send packets from UCL to California. And Sylvia B. Wilbur sends email from UCL to UK
 - 1974 TCP/IP by  Vint Cerf and Bob Kahn
    - TCP-Transmission Control Protocol (how do the packets get there?)
    - IP-Internet Protocol (manages addressing)
- 1970s had RCOnet, METROnet and MIDnet pop up in th UK
- 1979 Micronet allows access to computing services on dial-up with 1000 users in 1980

###  Commercialisation (1980s)
- 1981 USENET and other small networks with various protocols
- 1982 CSNET in the US with 24 sites
- 1983 ARPANET moves from NCP to TCP/IP and is split into MILNET (operational) and ARPANET (research)
- 1984 JANET created in UK for academic needs (starting to use .uk and other country domains)
- 1986 NSFNET launched in US
- 1989 First commercial ISP


## WEB 1.0 to Society 5.0
- Web 1.0 (The Static Web (read only Web) late 1980s-Early 2000s)
- Web 2.0 (The Social Web (read/write Web) mid 2000s- Early 2010s (but also present))
- Web 3.0 (The Semantic Web, Early 2010s-present)
- Web 4.0 (The Symbiotic Web, Conceptual/Future)
- Society 5.0 (A Human-Centric Super Smart Society)

### Web 1.0
- 1990/1991 Sir Tim Berners Lee credited with inventing World Wide Web, the first browser, and fundamental protocols and algorithms allowing web to scale. And got Touring Award for it.
- 1990 first server and browser
- 1991 first web server outside Europe
- 1993 HTML 1.0
- 1994 W3C created
- 1996 HTTP 1.0 standart
- Web 1.0 features:
    - Static HTML pages
    - Read only Web
    - Established Internet as 'informational space'
    - Minimal interaction, you just went onto internet to obtain information
    - Lectures

### Web 2.0
- 1997 HTTP 1.1
- 1999 AJAX
- 2000 RESTful APIs
- 2003 Wordpress
- 2004 Facebook
- 2006 JSON 'informational specification'
- Features:
    - Read/Write (web forms and such)
    - Peer to Peer
    - XML, RSS
    - APIs
    - Broadband 
    - Conversation

### Web 3.0
- Working to define a logical structure and ontology for the web so automated reasoning can take place over data
- RDF, OWL, SPARQL
- 1999 W3C RDF specification
- 2004 OWL 1 specification
- 2006 TBL 'the simple idea is largely unrealised'
- 2009 OWL 2 specification
- 2009 Bitcoin
- 2014 Web3 as a blockchain driven decentralised ecosystem

### Web 4.0
- Humans and machines
- Read/Write/Execute
- AI generated content and agents etc.

### Society 5.0 
- Super smart society where technology serves humans
- Enhance human life across various dimensions
    - Social welfare
    - Economic advancement
    - Environmental sustainability
- "Internet as if people mattered" as opposed to just being a resource for information harvesting.

## The internet today

- Impact of social media:
    - Rapid spread of [mis/dis]information
    - Privacy concerns
    - Impact on mental health
    - And some good things, perhaps...
- Cybersecurity:
    - Cyber attacks
    - Data breaches, ransomware
    - How to protect personal information
- Future trends:
    - 5G -> 6G (everything is connected)
    - Io(every)T
    - AI
    - Metaverse (didn't really pick up, did it tho?)
    -What will internet look like and how will we use it?

## The Client-Server concept and need for protocols
- How to get resource from one place to another?
    - Server (has the thing) --> Client (asks for the thing)
    - Client --(request)--> Server --(response)--> Client
    - Questions to ask: 
        - Where is the server?
        - Which file is it?
        - Where is the client?
        - What is the client?

- Client and server roles
- The need of protocols
    - Gopher (old, ancient)
    - FTP (File Tranfer Protocol), still in use for moving files around
    - HTTP, protocol of WWW
- Questions to ask client
- Examples of clients and servers
    -Clients:
        - Web browsers
        - Curl
        - Telnet
        - Libraries for programming languages to design clients
        - Apache
        - Nginx
        - IIS
        - VSC live mode

## The HTTP protocol
- https is just encrypted http
- The GET method
    - GET pulls information off server
    - Telnet-allows to genereate HTTP requests with URL and port (pot is usually 80)
        ```
        >>>telnet www.london.uc.uk 80
        (connects to server)
        >>>GET /
        (asks for top page)
        ```
    - Curl (bit more sophisticated than telnet, uses HTTP)
        ```
        >>>curl https://www.london.ac.uk
        (connects to server and fetches page)
        ```
    - Or just access through browser
    - From Server perspective:
        - Run command line server
        - Observe incoming requests
- Status codes:
    - 200 -OK
    - 404 File not found
    - 500 Server error\
- POST method does the opposite of GET, it pushes information on to the server

## Statelessness, cookies and HTTP
- HTTP is stateless, it doesnt store session information itself. So any new session starts from nothing, as there is no information stored in basic HTTP protocol.
- Things that cannot be done without state:
    - Remembering logins
    - Remembering shopping baskets
    - Tracking for targeted ads
- ### Cookies:
    - Small pieces of data stored on clients device, put there by a websiite. Used to track session information, personalise user experience and store login credentials.
    - Cookies create sort of an statefulness on top of HTTP
    - Cookie thieves can potentially intercept cookie being sent to a client by server, and then use it to impersonate client, especially with HTTP where packets are sent over network in plaintext. **HTTPS sends packets as encrypted packets.**