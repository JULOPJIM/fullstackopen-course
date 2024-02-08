sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Ingresar a https://studies.cs.helsinki.fi/exampleapp/notes
    Browser->>Server: GET /exampleapp/notes
    Server-->>Browser: Retorna la página de Notas (HTML, CSS, JS)
    Browser->>User: Muestra la página de Notas

