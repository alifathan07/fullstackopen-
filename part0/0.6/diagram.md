
```mermaid
sequenceDiagram
    participant user
    participant browser
    participant server

    user->>browser: Writes a note and clicks Save

    browser->>server: POST /new_note_spa with note data as JSON
    activate server
    server-->>browser: 201 Created
    deactivate server

    browser->>browser: JavaScript updates the DOM
    browser-->>user: New note appears