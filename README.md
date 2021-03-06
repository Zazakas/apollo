# Apollo

```
We choose to go to the moon in this decade and do the other things,
not because they are easy, but because they are hard.
-- John F. Kennedy, 1962
```

Welcome to the Apollo GitHub.

[Apollo](http://apollo.auto) is an open autonomous driving platform. It is a high performance flexible architecture which supports fully autonomous driving capabilities.


## Installation

We strongly recommend building Apollo in our pre-specified Docker environment.
See the following instructions on how to set up the docker environment and build from source.

### The docker environment can be set by the commands below.

```
bash docker/scripts/install_docker.sh
# logout and login to make sure to run docker command without sudo
docker ps  # to verify docker works without sudo
bash docker/scripts/dev_start.sh
bash docker/scripts/dev_into.sh
```
### To build from source

```
bash apollo.sh build
```

## Run Apollo
Follow the steps below to launch Apollo:
### Start Apollo
```
# start Human Machine Interface(HMI)
bash scripts/hmi.sh
```
### Access HMI
Access HMI by opening your favorite browser, e.g. Chrome, go to http://localhost:8887, click Dreamview to start.
![HMI Enable Dreamview](docs/demo_guide/images/dreamview_enable.png)


Click upper-right Dreamview button
![HMI Launch Dreamview](docs/demo_guide/images/dreamview_launch.png)

to load Dreamview UI.

![Open Dreamview](docs/quickstart/images/hmi_open_dreamview.png)

### Replay demo rosbag
```
# in a different terminal, in the apollo directory
bash docker/scripts/dev_into.sh # jump into the docker container
rosbag play -l ./docs/demo_guide/demo.bag
```
Dreamview should show a running vehicle with trajectory now.
![Dreamview with Trajectory](docs/demo_guide/images/dv_trajectory.png)

Advanced users who wish to build outside this Docker container can refer
to the corresponding Docker specification file (`./docker/dev.dockerfile`).

## Documents
Apollo documents can be found under the [docs](https://github.com/ApolloAuto/apollo/blob/master/docs/) repository.
   * [quickstart](https://github.com/ApolloAuto/apollo/blob/master/docs/quickstart/): the quickstart tutorial.
   * [demo_guide](https://github.com/ApolloAuto/apollo/blob/master/docs/demo_guide/): the guide for demonstration.
   * [![Apollo Offline Demo](https://img.youtube.com/vi/Q4BawiLWl8c/0.jpg)](https://www.youtube.com/watch?v=Q4BawiLWl8c)
   * [how to contribute code](https://github.com/ApolloAuto/apollo/blob/master/CONTRIBUTING.md): the guide for contributing code to Apollo.
   * [howto](https://github.com/ApolloAuto/apollo/blob/master/docs/howto/): tutorials on how to build, run and modify codes.
   * [specs](https://github.com/ApolloAuto/apollo/blob/master/docs/specs/): Specification documents of Apollo 1.0.

## Ask Questions

You are welcome to submit questions and bug reports as [Github Issues](https://github.com/ApolloAuto/apollo/issues).

## Copyright and License
Apollo is provided under the [Apache-2.0 license](LICENSE).

## Disclaimer
Please refer the Disclaimer of Apollo in [Apollo official website](http://apollo.auto/docs/disclaimer.html).
