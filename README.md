# Experiment:Time Table

## AIM:
To Write a HTML Webpage to Display First Semester TimeTable.

# ALGORITHM:

### STEP 1:
Create a Simple Table using Table Tag.

### STEP 2:
Add Header Row using th Tag.

### STEP 3:
Add First Semester TimeTable.

### STEP 4:
Execute the program.

# CODE:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>TIMETABLE</title>
</head>
<body style="background-color:lavender">
<img src="https://www.saveetha.ac.in/images/WEB_LOGO-01.png" width="100%" height="200">
<h1 style="text-align:center;">FIRST SEMESTER TIMETABLE</h1>

<table border="1" cellspacing="1" bordercolor="black" bgcolor="lavenderblush" width="100%">
    
    <tr>
        <th colspan="8" height="40px" style="background-color:lightcyan">TIME TABLE</th>
    </tr>
    <tr bgcolor="honeydew">
        <th colspan="4" height="40px">NAME:RITHIGA SRI.B</th>
        <th colspan="8" height="40px">REFERENCE NO:21500732</th>
    </tr>
    <tr height="40px">
        
        <th style="background-color:yellow">DAY</th>
        <th style="background-color:yellow">1</th>
        <th style="background-color:yellow">2</th>
        <th style="background-color:yellow">3</th>
        <th style="background-color:yellow">4</th>
        <th rowspan="6" bgcolor="cornsilk">LUNCH BREAK</th>
        <th style="background-color:yellow">5</th>
        <th style="background-color:yellow">6</th>
    </tr>
    <tr height="40px" style="text-align:center;">
        <td style="background-color:palegreen">MONDAY</td>
        <td colspan="2">Fundamentals of Web Technology</td>
        <td colspan="2">Linear Algebra Laboratory</td>
        <td colspan="2">Mathematics for Artificial Intelligence</td>
    </tr>
    <tr height="40px" style="text-align:center;">
        <td style="background-color:palegreen">TUESDAY</td>
        <td colspan="2">Free Time</td>
        <td colspan="2">Engineering Design and Modeling</td>
        <td colspan="2">Engineering Mechanics and Product Development</td>
    </tr>
    <tr height="40px" style="text-align:center;">
        <td style="background-color:palegreen">WEDNESDAY</td>
        <td colspan="2">Soft Skills</td>
        <td colspan="2">Python Programming</td>
        <td colspan="2">Fundamentals of Web Technology</td>
    </tr>
    <tr height="40px" style="text-align:center;">
        <td style="background-color:palegreen">THURSDAY</td>
        <td colspan="2">Engineering Mechanics and Product Development</td>
        <td colspan="2">Python Programming</td>
        <td colspan="2">Engineering Design and Modeling</td>
    </tr>
    <tr height="40px" style="text-align:center;">
        <td style="background-color:palegreen">FRIDAY</td>
        <td colspan="2">Free Time</td>
        <td colspan="2">Mathematics for Artificial Intelligence</td>
        <td colspan="2">Web Technology Laboratory</td>
    </tr>

</table>
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
```

# OUPUT:

## CLIENT SIDE OUTPUT:
![Output 1](./Images/Output1.png)

## SERVER SIDE OUTPUT:
![Output 2](./Images/Output2.png)


