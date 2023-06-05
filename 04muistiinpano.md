```mermaid
sequenceDiagram
	participant browser
	participant server
	
	browser->>server: Request URL: https://studies.cs.helsinki.fi/exampleapp/new_note method POST
	activate server
	server-->>browser: 302: redirect
	deactivate server
	
	Note right of browser: form data is sent with HTTP POST

	browser->>server: Request URL: https://studies.cs.helsinki.fi/exampleapp/notes method GET
	activate server
	server-->>browser: HTML document
	deactivate server

	browser->>server: Request URL: https://studies.cs.helsinki.fi/exampleapp/main.css method GET
	activate server
	server-->>browser: the css file
	deactivate server

	browser->>server: REquest URL: https://studies.cs.helsinki.fi/exampleapp/main.js method GET
	activate server
	server-->>browser: the JavaScript file
	deactivate server

	Note right of browser: browser starts executing the JavaScript code that fetches the JSON from the server

	browser->>server: Request URL: https://studies.cs.helsinki.fi/exampleapp/data.json merthod GET
	activate server
	server-->>browser the data
	deactivate server
	
	Note right of browser: The browser executes the callback function that renders the notes
```
	
