<img src="https://raw.githubusercontent.com/PocketRelay/.github/main/assets/logo-new-text.svg" width="100%" height="160px">

# Pocket Relay

`Mass Effect 3 Multiplayer Emulation Project`

[Discord Server (https://discord.gg/yvycWW8RgR)](https://discord.gg/yvycWW8RgR)

Pocket Relay is a project which provides reverse engineered servers for Mass Effect 3 that emulate
the functionality of the official servers while being able to be hosted over lan. The current server
implementation is written in Kotlin because of SSL issues but those issues have been solved through my
[Blaze-ssl](https://github.com/jacobtread/blaze-ssl) project and the backend is currently being re-written
in Rust.

## Creating a server

If you would like to host a Pocket Relay server whether it be for LAN gaming or a community you can follow the
guide [Here](https://github.com/PocketRelay/.github/blob/main/manual/SETUP_SERVER.md)

## Connecting to a server

If you would like to connect to a Pocket Relay server or would like a guide to send to others on how to connect
to your server you can find that [Here](https://github.com/PocketRelay/.github/blob/main/manual/SETUP_CLIENT.md)

## Setting up Manager Software

For a guide to setting up your server to use with the [Manager](https://github.com/PocketRelay/PocketRelayManager) software
you can follow the guide [Here](https://github.com/PocketRelay/.github/blob/main/manual/MANAGER_SETUP.md)

## Compile Server 

If you would like to compile the server yourself from source you can follow [This](https://github.com/PocketRelay/.github/blob/main/manual/BUILDING.md) Guide


## Projects

### Server (https://github.com/PocketRelay/ServerRust)

This repository contains the Pocket Relay server implementaiton which is written in Rust

### Client (https://github.com/PocketRelay/Client)
The client application which configures client computers to be able to connect to the 
Pocket Relay server rather than the official servers.

### Manager (https://github.com/PocketRelay/PocketRelayManager)

This repository contains a seperate client used for managing Pocket Relay servers. It allows you to edit players, inventories, class levels, etc and view currently playing games

### Blaze SSL Async (https://github.com/jacobtread/blaze-ssl-async)

This is a custom implementation of the legacy SSLv3 protocol along with the 
TLS_RSA_WITH_RC4_128_SHA and TLS_RSA_WITH_RC4_128_MD5 cipher suites in order to 
support the required connections for gosredirector.ea.com. Common issue facing previous versions was finding support for this protocol and ciphers as due to how old it is most implementations require hacky solutions in order to enable it but this implementation is a pure rust implementation.

### Blaze SSL (https://github.com/jacobtread/blaze-ssl)

> Note: This is the syncronous version of Blaze SSL Async and is no longer maintained as its been superseeded by the asyncversion

This is a library which implements the SSLv3 protocol with the TLS_RSA_WITH_RC4_128_SHA cipher which is 
required for the first redirection step of emulating Mass Effect 3 servers. This is being created to 
replace hacky tweaks with SChannel / the Java JDK SSL

### BlazePK (https://github.com/jacobtread/BlazePK-rs)

This is a library which implements the Blaze packet system which Mass Effect 3 uses. This library
implements it in the Rust language. This library takes a encoding and decoding from structures 
approach when encoding packets

### BlazeKT (https://github.com/jacobtread/BlazeKt)

This is a library which implements the Blaze packet system which Mass Effect 3 uses. This library
implements it in the Kotlin language. This library takes a DSL / Typesafe builder approach when 
encoding packets

### Archived Kotlin Server (https://github.com/PocketRelay/ServerKotlin)
This is the previous implementation of the Pocket Relay server before the current Rust server. This
server is written in Kotlin and requires a JVM to run and will no longer recieve updates.

### RedirectorClient  (https://github.com/PocketRelay/RedirectorClient )

> Note: This client implementation is no longer used and the redirector logic has been moved back
> to the server side as it was not worth proxing all the extra data.

This is the new client written in Rust. This is apart of the new architecture which moves SSLv3 away from
the server and instead implements the redirector on the client side. This will be used with the Rust Server
when Blaze SSL is complete

The original proof of concept for this was written in Kotlin and is archived here https://github.com/PocketRelay/ClientKotlin

## EA / BioWare Notice
All code in this repository is authored by Jacobtread and none is taken from BioWare. This code has been 
produced from studying the protocol of the official servers and emulating its functionality. This program is in no way or form supported, endorsed, or provided by BioWare or Electronic Arts.
