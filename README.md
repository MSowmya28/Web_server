# Developing a Simple Webserver
## AIM:

To develop a simple webserver to serve html pages.
## DESIGN STEPS:
### Step 1:

HTML content creation
### Step 2:

Design of webserver workflow
### Step 3:

Implementation using Python code
### Step 4:

Serving the HTML pages.
### Step 5:

Testing the webserver
## PROGRAM:
[8:20 AM, 12/1/2021] Jithu❤️: <!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>Name:Sowmya.M</h1>
<h2>21005357</h2>
<h2>Artificial inteligence and data science</h2>
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

## OUTPUT:
![output](https://github.com/MSowmya28/Web_server/blob/main/output.png?raw=true)
## RESULT:
The program is exected.
