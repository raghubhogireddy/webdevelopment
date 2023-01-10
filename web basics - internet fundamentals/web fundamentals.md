## DNS
DNS - Domain Name System 
- job is to convert the readable domain name to IP(Internet Protocol) Address 
- 2 Ways your computer get DNS 
   - either your ISP provide the DNS
   - you can manually configure the DNS

How DNS resolve the domain Name to IP ? 
- DNS will do something called Domain name Resolution where it does following steps
    - Requesting web site information in local cache
    - Contact recursive DNS servers
    - Query Authorative DNS Servers
    - Access the DNS record
    - reads IP Address from the DNS record and pass to browser and also record in local cache.

## HTTP respone status code

HTTP response status code indicate whether a specific HTTP request has been successfully completed. Responses are grouped into five classes.
_1XX Informational_

| Status Code | Reason Phrase | Description |
|-------------|---------------|-------------|
| 100 | Continue | The server received the request headers and should continue to send the request body. |
| 101 | Switching Protocols | The client has requested the server to switch protocols and the server has agreed to do so. |

_2XX Successful_

| Status Code | Reason Phrase | Description |
|-------------|---------------|-------------|
| 200 | OK | Standard response returned by the server to indicate it successfully processed the request. |
| 201 | Created | The server successfully processed the request and a resource was created. |
| 202 | Accepted | The server accepted the request for processing but the processing has not yet been completed. |
| 204 | No Content | The server successfully processed the request but is not returning any content. |

_3XX Redirection_

| Status Code | Reason Phrase | Description |
|-------------|---------------|-------------|
| 301 | Moved Permanently | This request and all future requests should be sent to the returned location. |
| 302 | Found | This request should be sent to the returned location. |

_4XX Client Error_

| Status Code | Reason Phrase | Description |
|-------------|---------------|-------------|
| 400 | Bad Request | The server cannot process the request due to a client error, e.g., invalid request or transmitted data is too large. |
| 401 | Unauthorized | The client making the request is unauthorized and should authenticate. |
| 403 | Forbidden | The request was valid but the server is refusing to process it. This is usually returned due to the client having insufficient permissions for the website, e.g., requesting an administrator action but the user is not an administrator. |
| 404 | Not Found | The server did not find the requested resource. |
| 405 | Method Not Allowed | The web server does not support the HTTP method used. |

_5XX Server Error_

| Status Code | Reason Phrase | Description |
|-------------|---------------|-------------|
| 500 | Internal Server Error | A generic error status code given when an unexpected error or condition occurred while processing the request. |
| 502 | Bad Gateway | The web server received an invalid response from the Application Server. |
| 503 | Service Unavailable | The web server cannot process the request. |

## Port Numbers
Your computer runs multiple services at one time and these services are listening to different ports at same time to serve the incoming requests. 
Port numbers under 1023 (i.e. from 0 to 1023) are privileged ports. That means they require certain administrative access to be "opened"
There are some port numbers reserved for certain operations. Although you can change them, but they still technically are popular choices. For example, HTTP runs on port 80 (or 8080), HTTPS on port 443 (or 8443). SSH runs on port 22. DNS runs on port 53, and so on.
Port numbers are not infinite.
You have a finite number of ports, and the range of ports is from 0 to 65535. This means you cannot start a process on port number 70000 (as it is outside the valid port range)

## HTTP Methods

HTTP methods indicate the action that the client wishes to perform on the web server resource.

Common HTTP methods are:

| HTTP Method | Description |
|-------------|-------------|
| GET | The client requests a resource on the web server. |
| POST | The client submits data to a resource on the web server. |
| PUT | The client create  a resource on the web server. |
| DELETE | The client deletes a resource on the web server. |

## HTTP Request headers

```
Host: example.com​
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: */*
Accept-Language: en​
Content-type: text/json
```

- The `Host` header specifies the host of the server and indicates where the resource is requested from.

- The `User-Agent` header informs the web server of the application that is making the request. It often includes the operating system (Windows, Mac, Linux), version and application vendor.

- The `Accept` header informs the web server what type of content the client will accept as the response.

- The `Accept-Language` header indicates the language and optionally the locale that the client prefers.

- The `Content-type` header indicates the type of content being transmitted in the request body.