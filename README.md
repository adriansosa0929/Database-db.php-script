schtasks /create /tn "FlaskServer" /tr "cmd /c cd C:\inetpub\wwwroot && python server.py" /sc onstart /ru SYSTEM /f
schtasks /query /tn "FlaskServer"
