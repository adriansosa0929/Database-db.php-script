sc create FlaskServer binpath= "C:\Users\itadmin\AppData\Local\Python\pythoncore-3.14-64\python.exe C:\inetpub\wwwroot\server.py" start= auto
sc start FlaskServer
sc query FlaskServer
