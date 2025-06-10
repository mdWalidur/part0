sequenceDiagram
    participant browser
    participant server

    Note right of browser: User types a new note and clicks "Save"

    browser->>server: POST /new_note_spa
    activate server
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: Browser updates the notes list without reloading the page
