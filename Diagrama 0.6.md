```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: El servidor guarda la nueva nota
    server-->>browser: Respuesta con el JSON actualizado
    deactivate server

    Note right of browser: El navegador actualiza la lista de notas sin recargar la página
