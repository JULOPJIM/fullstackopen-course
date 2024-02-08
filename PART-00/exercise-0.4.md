sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Ingresar a https://studies.cs.helsinki.fi/exampleapp/notes
    Browser->>Server: GET /exampleapp/notes
    Server-->>Browser: Retorna la página de Notas (HTML, CSS, JS)
    Browser->>User: Muestra la página de Notas

    User->>Browser: Completa el formulario para agregar una nueva nota
    Browser->>Server: POST /exampleapp/new_note {note: "Contenido de la nueva nota"}
    Server-->>Browser: 302 Found (Redirección a /exampleapp/notes)
    Browser->>Server: GET /exampleapp/notes
    Server-->>Browser: Retorna la página de Notas actualizada (HTML, CSS, JS)
    Browser->>User: Muestra la página de Notas actualizada
