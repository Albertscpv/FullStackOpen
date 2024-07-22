sequenceDiagram
  participant browser
  participant server

  browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server-->browser: HTML document
  desactivate server
  
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server-->browser: HTML document
  desactivate server
  
  browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server-->browser: css file
  desactivate server

  browser-->server GET https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server--> browser: JS file
  desactivate server

  browser-->server GET https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server--> browser: [{"content": "New note", "date": "new Date()", ... }]
  desactivate server
  
  
