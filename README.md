# Developing a Simple Webserver
Name : Vamsi Krishna G\
Reference No. : 23006287

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
</body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8007)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
## OUTPUT:

### serveroutput:
![serveroutput](https://github.com/vamsikrishna272005/webserver/assets/147477015/d912d938-1d83-4f69-88ba-b804ebbbe765)


### clientouput:
![clientoutput](https://github.com/vamsikrishna272005/webserver/assets/147477015/5506959d-c4fe-47f8-8cdb-b0efc30121c0)


## RESULT:
The program is executed succesfully
