### Part One: Solidify Terminology

1. What is HTTP: The Hypertext Transfer Protocol is standard in which browers and servers communicate. 
2. What is a URL: The URL is a string that contains the information needed to connect to a specific server including its IP address, the protocol for reaching the address, the port through which it*, and the resource and query. 
3. What is a DNS: The Domain Name Service is a supercomputer that provides the global IP address of given hostname. The DNS are located geographically around the world, and the one we connect to are not within our power.
4. What is a Query String: The query string provides information about the webpage that is exterior of the resources. It is frequently used to hold search terms or information from non-secure forms. 
5. What are two HTTP verbs and how are they different: The two "verbs" are GET and POST, which are methods by which we specify whether we want the request we make to change the data on the server. GET is used for requests that don't the webpage to change its data, whereas POST is used for requests that requre the webpage to change its data. 
6. What is HTTP Request: An HTTP Request is the action in which the browser requests information from a server. 
7. What is HTTP Response: An HTTP Response is the action in which the server provides to the browser the information that was requested. At times, the server may make its own request to a DB server, which will provide a response to the server, and then back to our browser. 
8. What is an HTTP Header: The Header is the meta-data included in HTTP Requests and Responses. Examples include the language that the browser is using, time that request/response was made/sent, and operating software. 
9. What are the processes that happen when you type “http://somesite.com/some/page.html” into a browser: 1) It defines the protocol as "HTTP" 2) the browser translate the hostname "somesite.com" to an IP address 3) the default port 80 will be selected 4) the resource string "some/page.html" is used to find the target file. 

### Part Two: Practice Tools
1. Using curl, make a GET request to the icanhazdadjoke.com API to find all jokes involving the word “pirate”
API: https://icanhazdadjoke.com/api

Terminal: curl -H "Accept: application/json" "https://icanhazdadjoke.com/search?term=pirate"

Output: `{"current_page":1,"limit":20,"next_page":1,"previous_page":1,"results":[{"id":"QuscibaMClb","joke":"What does a pirate pay for his corn? A buccaneer!"},{"id":"2gii3LeN7Ed","joke":"Why couldn't the kid see the pirate movie? Because it was rated arrr!"},{"id":"SvzIBAQS0Dd","joke":"What did the pirate say on his 80th birthday? Aye Matey!"},{"id":"SnOf2gqjiqc","joke":"Why are pirates called pirates? Because they arrr!"},{"id":"exXSCtkOKe","joke":"Why do pirates not know the alphabet? They always get stuck at \"C\"."}],"search_term":"pirate","status":200,"total_jokes":5,"total_pages":1}`

2. Use dig to find what the IP address is for icanhazdadjoke.com

Terminal: dig icanhazdadjoke.com

Output: 

icanhazdadjoke.com.	229	IN	A	104.27.179.209
icanhazdadjoke.com.	229	IN	A	104.27.178.209

3. Make a simple web page and serve it using python3 -m http.server. Visit the page in a browser.
(See index.html)