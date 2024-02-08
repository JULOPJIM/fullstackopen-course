sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Interactúa con la página de Notas
    Browser->>User: Muestra la página de Notas (HTML, CSS, JS)
    
    User->>Browser: Completa el formulario para agregar una nueva nota
    Browser->>User: Interfaz de usuario actualizada para reflejar la nueva nota

    Browser->>Server: POST /exampleapp/new_note_spa {note: "Contenido de la nueva nota"}
    Server-->>Browser: 201 Created (Nota agregada exitosamente)

    Browser->>User: Muestra mensaje de confirmación o actualiza la interfaz con la nueva nota
