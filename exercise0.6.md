title New Note- Single page app

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
note over server: 
This POST request contains the new note as JSON-data 
containing both the content of the note and the date.
end note 

note over server:
Javascript code is now executed 
and the new note is sent to the server.
end note

server-->browser: status code 201 created
