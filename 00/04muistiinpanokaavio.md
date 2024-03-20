sequenceDiagram
	participant browser
	participant server
	
	browser->>server SEND data from form and HTTP POST
	activate server
	server-->>browser HTTP 302 redirectaus
	browser-->>server uudestaan HTTP GET, ladataan sivu uudelleen
	server-->>browser palvelin luo uuden olion ja lisää sen listaan
	server-->>browser selain latautuu uudestaan jolloin uudet muistiinpanot latautuvat
	deactivate server
