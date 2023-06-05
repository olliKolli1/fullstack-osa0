```mermaid
sequenceDiagram
	participant browser
	participant server

	browser->>server: request URL https://studies.cs.helsinki.fi/exapmleapp/spa method GET
	arctivate server
	server-->>browser: HTML document
	deactivate server
	
	browser->>server: Request URL https://studies.cs.helsinki.fi/exampleapp/main.css method GET
	activate server
	server-->>browser: the css file
	deactivate server
	
	browser->>server: Request URL https://studies.cs.helsinki.fi/exampleapp/spa.js method GET
	activate server
	server-->>browser: the JavaScript file
	deactivate server

	Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

	browser->>server: Request URL https://studies.cs.helsinki.fi/exampleapp/data.json method GET
	activate server
	server-->>browser: The data of the notes in JSON-form
	deactivate server
	
	Note right of browser: The browser executes the callback function that renders the notes
```
