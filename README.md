# About

This project runs a paper minecraft server and a "rathole" in two docker containers allowing the server to be accessed from outside the network without needing port forwarding. This requires that you have a VPS server with a public facing IP address that will act as a reverse proxy.

# Quick Start

- Download the `compose.yml` file and the `config.toml` onto the box that will be running the minecraft server
- Replace the all caps IP in `config.toml` with the public address of your VPS
- Place the two files into an empty directory of your choosing
- Run `docker-compose up -d` inside that directory
- On the VPS, follow the rathole quick start guide ([here](https://github.com/rapiz1/rathole/))
- Use the `rathole.toml` file as the rathole config on the server
- Replace the all caps IP in `rathole.toml` with the public address of your VPS
- Ensure that ports `1026/tcp` and `1028/tcp` are open on the VPS, and port `1028/tcp` is open on the client
- The server should be running on `VPSIP:1026`
