![Logo](../assets/logo.png)

# Pocket Relay

`Mass Effect 3 Multiplayer Emulation Project`

Pocket Relay is a project which provides reverse engineered servers for Mass Effect 3 that emulate
the functionality of the official servers while being able to be hosted over lan. The current server
implementation is written in Kotlin because of SSL issues but once those have been solved through my
[Blaze-ssl](https://github.com/jacobtread/blaze-ssl) project the backend will be re-written in Rust

## Projects

### Blaze SSL (https://github.com/jacobtread/blaze-ssl)

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

### Kotlin Server (https://github.com/PocketRelay/ServerKotlin)
This is the current working server that runs on the JVM and is written in Kotlin.


### Client (https://github.com/PocketRelay/Client)
This is the new client written in Rust. This is apart of the new architecture which moves SSLv3 away from
the server and instead implements the redirector on the client side. This will be used with the Rust Server
when Blaze SSL is complete

The original proof of concept for this was written in Kotlin and is archived here https://github.com/PocketRelay/ClientKotlin

### Rust Server (https://github.com/PocketRelay/ServerRust)

This is the repository where the future Rust server implementation will be located.