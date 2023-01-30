# Developing a simple web server

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:



### Step 4:

Serving the HTML pages.

base) sec@sec-HP-250-15-6-inch-G9-Notebook-PC:~/myproject/webserver$ python3 webserver.py
my webserver is running....
request received

### Step 5:

Testing the webserver


## PROGRAM:

Implementation using Python code
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<head>
<title>Django</title>
</head>
<body>

<h1>Django</h1>
<p>This is Web Application Framework written in python</p>

</body>
</html>
"""

class myhandler(BaseHTTPRequestHandler):
     def do_GET(self):
         print("request received")
         self.send_response(200)
         self.send_header('content-type','text/html; charset=utf-8')
         self.end_headers()
         self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running....")
httpd.serve_forever()
```

## OUTPUT:

### Server side output

![serveroutput](https://user-images.githubusercontent.com/119479566/215524495-28dad1c8-9dbb-4441-b50d-5933f95a9f24.png)


### Client side output

![clientoutput](https://user-images.githubusercontent.com/119479566/215524750-1c403454-01cc-41a7-8b76-f0887e87c215.png)

## RESULT:

The program is executed succesfully
