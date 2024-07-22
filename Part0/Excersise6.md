```mermaid
sequenceDiagram
  participant browser
  participant server


  %%Get current notes
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server-->>browser: spa file
  deactivate server

  %%Post new notes
  browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server-->>browser: {"message": "added"}
  deactivate server


  %%Get updated notes
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
  activate server
  server->>browser: [{"content": "note updated", "date": " hh/mm/yy "...}]
  deactive server


```
