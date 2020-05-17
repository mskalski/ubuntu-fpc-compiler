***Pull builder image and compile transgui***

```
git clone https://github.com/transmission-remote-gui/transgui.git source-code
docker run -itv `pwd`/source-code:/source-code andrewbeam/ubuntu-fpc-compiler:19.10
>> make clean && lazbuild -B transgui.lpi && make && make zipdist
>> exit
ls source-code/Release
```

***Build own builder image and compile transgui***

```
git clone https://github.com/transmission-remote-gui/transgui.git source-code
docker-compose build ubuntu-fpc-compiler-19.10
docker-compose run ubuntu-fpc-compiler-19.10
>> make clean && lazbuild -B transgui.lpi && make && make zipdist
>> exit
ls source-code/Release
```

***Links***

https://github.com/beam/ubuntu-fpc-compiler

https://hub.docker.com/repository/docker/andrewbeam/ubuntu-fpc-compiler
