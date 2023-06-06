```mermaid
sequenceDiagram
	participant browser
	participant server
	
	browser->>server: Request URL https://studies.cs.helsinki.fi/exampleapp/new_note_spa method POST
	activate server
	Note right of browser: The new note is posted to the server in JSON-form 
	deactivate server
	
	Note right of browser: The browser stays on the same page and no new requests happen
```
