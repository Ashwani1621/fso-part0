sequenceDiagram
    participant Browser
    participant Server

    Browser->>Server: POST /new_note (form data)
    Note right of Server: Server reads req.body.note\nAdds note to array
    Server-->>Browser: 302 Redirect to /notes

    Browser->>Server: GET /notes
    Server-->>Browser: HTML (Notes page)

    Browser->>Server: GET /main.css
    Server-->>Browser: CSS file

    Browser->>Server: GET /main.js
    Server-->>Browser: JavaScript file

    Browser->>Server: GET /data.json
    Server-->>Browser: JSON (notes data)
