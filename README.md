# Visual Studio in a container
NOTE: Needs /dev/dri


```bash
docker run -d \
   -v /tmp/.X11-unix:/tmp/.X11-unix \
   -v /home/$USER/workspace:/home/user \
   -e DISPLAY=unix$DISPLAY \
   --device /dev/dri \
   --name vscode \
   limezest/vscode
```
## start.sh
```bash
  #!/bin/bash
  su user -c /usr/local/bin/code
```
