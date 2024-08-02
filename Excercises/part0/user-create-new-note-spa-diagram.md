sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/example/new_note_spa
    {"content": "hi","date": "2024-08-02T14:22:19.174Z"}
    activate server
    server-->> browser: {"message": "note created"}
    desactivate server

    Note right of browser: At the time the js code insert the message on the DOM, the server is saving the message on the server.. 
