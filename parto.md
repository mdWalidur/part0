sequenceDiagram
    participant browser
    participant server

    browser->>server: GET /notes
    activate server
    server-->>browser: HTML document
    deactivate server

    Note right of browser: User types a new note into the text field

    browser->>server: POST /new_note
    activate server
    server-->>browser: Redirect to /notes
    deactivate server

    browser->>server: GET /notes
    activate server
    server-->>browser: Updated HTML document
    deactivate server
