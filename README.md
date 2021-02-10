Ubuntu 20.04 docker image.

```
git clone https://github.com/hirotakaster/pico-docker
cd pico-docker
docker-compose build
docker-compose up -d
```

Start up pico container with VScode Remote Container.
```
cd work
git clone https://github.com/raspberrypi/pico-setup
pico-setup/pico_setupt.sh
```

build own project(or sample) on VScode, you could find pico image on host dir(pico/work/...etc) .
