## docker-openbox-novnc

This is a minimal Docker installation with:
- Openbox on Ubuntu Server 16.04
- x11vnc server with NoVNC for remote access

Note: The WebSocket connections are encrypted and the URL is accessible only through HTTPS. As the generated SSL certificate is self-signed, it must be [recognized by the browser](https://github.com/novnc/websockify/wiki/Encrypted-Connections#accepting-a-self-signed-certificate-in-the-browser).

### Build
```docker build -t naei/openbox-novnc .```  

### Run
```docker run -id -p 6080:6080 -e VNC_PASSWD=<YourPassword> naei/openbox-novnc```  
The `-e VNC_PASSWD=<YourPassword>` parameter is optionnal. If not set, the VNC session will be accessible by everyone.

The system is accessible from: https://<YOUR_SERVER_IP>:6080
