### To build image
``docker build -t mrtkprc/my-custom-app .``

### To publish docker registry

``docker push mrtkprc/my-custom-app``

### CMD Instruction 

Sample Docker File
```

FROM Ubuntu

CMD sleep 5

```

``docker run ubuntu sleep 10``

Above code override Docker file CMD command.

### ENTRYPOINT

``` 

FROM Ubuntu

ENTRYPOINT ["sleep"]

```

``docker run my_ubuntu 10``

equals 

``docker run my_ubuntu sleep 10``

ENTRYPOINT defines constant command.

### ENTRYPOINT and CMD together usage

```
FROM Ubuntu

ENTRYPOINT ["sleep"]

CMD ["5"]
```

equals

``docker run my_ubuntu sleep 5``

However; we can override 5 by using command. For instance,

``docker run my_ubuntu 10``


However, we actually use another entrypoint,

``docker run --entrypoint my_sleep my_ubuntu 10``

### Define network

Network can be defined with option ``--network`` 
-   bridge
-   none
-   host


