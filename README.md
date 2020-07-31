<h1 align="center">STEAMCMD</h1>

<div align="center">
<image src="https://3.bp.blogspot.com/-Jbo2ByKvK60/VoFsdmqP4mI/AAAAAAAAIxk/Ahz__bJjweU/s1600/Logo%2BSteam.png" width="50%" />
</div>
<div align="center">
  Docker <code>alpine</code> image
</div>

<br />

<div align="center">
  <!-- Docker Build -->
  <a href="#">
    <img src="https://img.shields.io/docker/build/codevski/steamcmd?style=for-the-badge&logo=docker"
      alt="Docker Build" />
  </a>
  <!-- Code Quality Status -->
  <a href="#">
    <img src="https://img.shields.io/scrutinizer/quality/g/codevski/steamcmd?style=for-the-badge&logo=appveyor"
      alt="Code Quality" />
  </a>
  
</div>

<div align="center">
  <sub>The little project that could. Built with ❤︎ by
  <a href="#">codevski</a> and
  <a href="/graphs/contributors">
    contributors
  </a>
</div>

# What is SteamCMD?
The Steam Console Client or [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD) is a command-line version of the Steam client. Its primary use is to install and update various dedicated servers available on Steam using a command-line interface. It works with games that use the SteamPipe content system. All games have been migrated from the deprecated HLDSUpdateTool to SteamCMD. This image can be used as a base image for Steam-based dedicated servers.

# How to use this image
Whilst it's recommended to use this image as a base image of other game servers, you can also run it in an interactive shell using the following command:
```
$ docker run -it --name=steamcmd codevski/steamcmd bash
$ ./home/steam/steamcmd/steamcmd.sh +login anonymous +force_install_dir /home/steam/squad-dedicated \
    +app_update 403240 +quit
```
This can prove useful if you are just looking to test a certain game server installation.

# Configuration
This image includes the nano text editor. The `steamcmd.sh` can be found at the following path: /home/steam/steamcmd

## Examples
Consult the following repositories for examples on how to base an image off of this one:
- https://hub.docker.com/r/cm2network/csgo/

# Image Variants:
The `steamcmd` images come in two flavors, each designed for a specific use case.

## steamcmd:latest
This is the defacto image. If you are unsure about what your needs are, you probably want to use this one. It is designed to be used as the base to build other images off of. This image's default user is steam, any command executed in a higher layer Dockerfile will therefor be executed as that user.
