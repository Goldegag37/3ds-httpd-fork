# 3ds-httpd
## A modular web server for your 3ds
### Path Handlers
#### Default Handler  
	- Path: /  
	- Description:  
		redirects to /sdcard/httpd/index.html
#### Favicon Handler  
	- Path: /favicon.ico  
	- Description:  
		Returns a hardcoded SVG favicon  
#### System Handler  
	- Path: /system/3ds/  
	- Description:  
		/system/3ds/exit - Exits app  
		/system/3ds/reboot - Reboots system  
#### SDMC Handler  
	- Path: /sdcard/  
	- Description:  
		Returns content of requested file in SD Card with content-type text/html, if file is missing returns 404. Path starts at SDMC root  
#### Memory R/W Handler  
	- Path: /readmem/ || /writemem/  
	- Description:  
		Reads and writes system memory. Honestly you're more likely to crash your 3DS. Check source code for details  
#### Encryption Handler  
	- Path: /crypt/  
	- Description:  
		Uses native AES Encryption/Decryption Algorithms to do CBC/CTR/CTM. Check source code for details.  
