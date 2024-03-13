# EX01 Developing a Simple Webserver
## Date: 13.03.2024
## Name: AKSHAI KHANNA D
## Roll no: 212223040010
## Dept: CSE

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
```
ffrom http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<title>software companies</title>
<body>
<table border="3" cellspacing="2" cellpadding="6">
<caption>Top 5 Revenue Generating Software Companies</caption>
<tr>
	<th>S.no</th>
	<th>Company</th>
	<th>Revenue</th>
</tr>
<tr>
	<td>1</td>
	<td>Microsoft</td>
	<td>65 Billion</td>
</tr>
<tr>
	<td>2</td>
	<td>Oracle</td>
	<td>29.6 Billion</td>
</tr>
<tr>
	<td>3</td>
	<td>IBM</td>
	<td>29.1 Billion</td>
</tr>
<tr>
	<td>4</td>
	<td>SAP</td>
	<td>6.4 Billion</td>
</tr>
<tr>
	<td>5</td>
	<td>Symantec</td>
	<td>5.6 Billion</td>
</tr>
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
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:

![Codeee](https://github.com/akshai07/simplewebserver/assets/152007451/d7f2a54b-5a28-4d22-86ae-27af3879fe47)

![000000](https://github.com/akshai07/simplewebserver/assets/152007451/202ab4e3-dfff-4d91-94c9-891d6e69d5c3)


## RESULT:
The program for implementing simple webserver is executed successfully.
