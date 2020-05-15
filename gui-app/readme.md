# To build program(firefox)

```
docker build -t mrtkprc/firefox .
```

# To start program(firefox)

```
docker run -ti --rm -e DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/home/developer/.Xauthority --net=host --pid=host --ipc=host mrtkprc/firefox
```