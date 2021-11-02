title New Note

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note

note over server: 
Server recieves form data from browser.
The action and method attributes define 
that submitting the form is done as an HTTP POST 
request to the address new_note.
end note

server-->browser: status code 302

note over browser: 
Server asks browser to do a new
HTTP GET request to the address defined 
in the header's Location - the address notes.
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
server-->browser: HTML-code
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
server-->browser: main.js

note over browser:
browser starts executing js-code
that requests JSON data from server 
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{"content":"j","date":"2021-10-31T12:29:53.581Z"}, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note