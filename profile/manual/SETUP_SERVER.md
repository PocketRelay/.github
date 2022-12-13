# Server Setup Guide

> This is the setup guide for setting up a Pocket Relay server. Servers can run on dedicated hosting, within docker or on your own computer.

If you are looking to configure the server such as changing different ports or other server data you can view the configuration guide [Here](https://github.com/PocketRelay/ServerRust/blob/master/docs/CONFIG.md)

## Executable

> This section is for if you are running the server directly from an executable. You can find a section for running the server within a Docker container at the bottom of this page [Here](#Docker)

### 1)  Download Executable

Pre compiled binary downloads are available below. But if you would like to compile from source manually see the [Manual Building](BUILDING.md) guide

You can view the latest server download [Here](https://github.com/PocketRelay/ServerRust/releases/latest) or you can directly download the release for your platform from one of the links below

| Platform | Download                                                                                                |
| -------- | ------------------------------------------------------------------------------------------------------- |
| Windows  | [Download](https://github.com/PocketRelay/ServerRust/releases/latest/download/pocket-relay-windows.exe) |
| Linux    | [Download](https://github.com/PocketRelay/ServerRust/releases/latest/download/pocket-relay-linux)       |


### 2) Move to own directory

Move the binary file to its own directory in order to not interfere with or overlap with other files and folders. All the Pocket Relay data files will be stored in a "data" folder alongside the executable.

### 3) Launching 

Next you can launch the executable. 

#### Windows
If you are on windows you can do this either by opening the executable normally with a Double Click or Right Click + Open or through the terminal using ``./pocket-relay.exe`` 

#### Linux
If you are on linux you will first need to make the executable "executable" you can do this with the following command

```shell
chmod +x ./pocket-relay
```

Then you can start the server with the following command

```shell
./pocket-relay
```

> Note with the default configuration you will need to run the `./pocket-relay` command as `sudo ./pocket-relay` as the default configuration uses port 80 for the HTTP server. If you are already running an Apache HTTP server or another app is using port 80 you will either need to change it
> in the configuration file to another port such as 8080 or 3000 or stop the other apps 

### 4) Connection URL

Now that your server is up and running the server will output the connection urls into the log. You can find this log in the terminal you are using to run the server or in the log file at `data/logs/log.log` the possible connection urls will be near the top of the log. You should see a message like the one below

```log
[2022-11-28T15:14:35.555306400+13:00 INFO pocket_relay] Connection URLS (LAN: 192.168.88.251, WAN: IP_REDACTED, LOCAL: 127.0.0.1)
```

The connections URLs are filtered by the interface and seperated with commas. Below is table showing which IP is which corresponds to which usage

| Name  | Description                                                                                                                                                     |
| ----- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| LAN   | If you are running this server over a Local Area Network and want someone to play with you on the same Network then give them this address                      |
| WAN   | If you are hosting this server publicly you can give this IP to others across the Internet to connect to you with (Note you must port forward for this to work) |
| LOCAL | This is the address you will use if you are connecting to a server running on your current machine (You can also use localhost instead)                         |

### 5) Futher Configuration 

In order to further configure your server and change different settings see [Here](https://github.com/PocketRelay/ServerRust/blob/master/docs/CONFIG.md). Ensure that you restart the server after changing any configuration settings in order for them to be applied correctly

## Docker

> This section is for users looking to run the server within a Docker container. If you aren't doing this keep scrolling to the next section

Optionally if you are using Docker you can use the following command to create a new Pocket Relay server from the docker image or configure a container in Docker Desktop for the `jacobtread/pocket-relay:latest` image

```shell
docker run -d -p 80:80/tcp -p 14219:14219/tcp -p 42127:42127/tcp jacobtread/pocket-relay:latest 
```

The `-p` arguments bind the ports for the servers running inside the image. The exposed port 42127 must always stay the same or else clients will be unable to connect to the server. 

> See the configuration guide for changing ports and other configuration
> [Here](https://github.com/PocketRelay/ServerRust/blob/master/docs/CONFIG.md)

