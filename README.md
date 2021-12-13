# Developing a Simple Webserver
## AIM:

To develop a simple webserver to serve html pages.
## DESIGN STEPS:
### Step 1:

HTML content creation.
### Step 2:

Design of webserver workflow.
### Step 3:

Implementation using Python code.
### Step 4:

Serving the HTML pages.
### Step 5:

Testing the webserver.
## PROGRAM:
~~~
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>Mywebserver</title>
</head>
<body>
<h1>Hari krishna</h1>
<h2>21002044</h2>
<h4>harikrishna242426@gmail.com</h4>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8080)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
~~~

## OUTPUT:
![OUTPUT](/IMAGES/img50.png)
## RESULT:
Thus the program to create web repository is completed sucessfully.