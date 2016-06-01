## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
- the protocol/scheme (HTTP or HTTPS)
- the host name (e.g., www.google.com)
- the file name (e.g., index.html)
<scheme>://<username>:<password>@<host>:<port>/<path>;<parameters>?<query>#<fragment>

* Name the pieces of the following urls:
	* `https://www.google.com/`
	 - protocol://hostName.topLevelDomain/
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367`
	 - protocol://subdomain.hostname.topLevelDomain/path
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy`
	 - protocol://hostName(local):port/path/parameters
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
	 - protocol://language.hostName/path
* Can a server use more than 1 port?
 - yes...ports can be dynamically assigned on a per request basis from a reserved pool of port numbers

* Why is https different than http?
- HTTPS works in conjunction with another protocol, Secure Sockets Layer (SSL), to transport data safely. HTTPS is secure because it uses SSL to move data and differentiates one sender and receiver from another.

* How does a server interpret the following url's query parameter?  What data structure does it create on the server?
- it searches in the animals file on the localhost on port 5000 for puppies(the key) with the
  values of fido, max, and moxie
-

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```

__HTTP Request/Response__

* Name at least 4 http verbs
- POST, GET, PUT, DELETE, and PATCH

* What is each verb useful for in your own words
- POST creates new data
- GET reads data
- PUT updates/replaces data
- DELETE deletes data
- PATCH updates/modifies data

* What does idempotent mean?
-  clients can make that same call repeatedly while producing the same result. In other words, making multiple identical requests has the same effect as making a single request. GET and PUT are idempotent. DELETE is idempotent if you are just marking the item for deletion instead of actually deleting it. If you do delete something for good, DELETE is not idempotent. POST is not idempotent.

* Name the 5 http status code ranges.  What are they used for in general?
- 100s: Informational
- 200s: Success
- 300s: Redirection
- 400s: Client Error
- 500s: Server Error

* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept
	* Content-type
	* User-agent
	* Set-cookies
	* Cache-control
	* Cookie
* Is the following a http request or response?  How do you know for each?

```
HTTP/1.1 200 OK
Access-Control-Allow-Origin: *
Vary: Accept
Content-Type: text/html; charset=utf-8
Content-Length: 722
ETag: W/"2d2-Wu0We9N5g35FXWY+gOATLA"
Date: Tue, 08 Mar 2016 20:37:11 GMT
Connection: keep-alive

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="/style.css">
    <title>Student Roster</title>
  </head>
  <body>
    <main>
      <h1>Student Roster</h1>

        <section>
          <h3>Daenerys Targaryen</h3>
          <span>Student Id: nys8fbohl</span>
          <h4>Hobby: Motherhood</h4>
          <img src="https://i.imgur.com/KlycRG5.jpg" alt="Daenerys Targaryen" />
        </section>

        <section>
          <h3>Tyrion Lannister</h3>
          <span>Student Id: njehukbohe</span>
          <h4>Hobby: Traveling</h4>
          <img src="https://i.imgur.com/fFMusdC.png" alt="Tyrion Lannister" />
        </section>

    </main>
  </body>
</html>
```

```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
```

__JSON__

* Describe what JSON is.  What is it used for.
* Convert the following map into a javascript object then console log the age.

```
{ "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}
```
* Convert the following to a javascript object.  Console log each company name.

```
{ "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}
```
* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};
```
__MISC__

* Describe what DNS is.
 - DNS is the Domain Name Server and maps domain names to IP addresses

* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).

* What is TCP/IP?  How does it interact with HTTP?
- TCP/IP is Transmission Control Protocol/Internet protocol

* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
