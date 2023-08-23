<img src="https://raw.githubusercontent.com/PocketRelay/.github/main/assets/logo-new-text.svg" width="100%" height="160px">

# Pocket Relay

`Mass Effect 3 Multiplayer Emulation Project`

[Website (pocket-relay.pages.dev/)](https://pocket-relay.pages.dev)

Pocket Relay is a project which provides reverse engineered servers for Mass Effect 3 that emulate
the functionality of the official servers while being able to be hosted over LAN. This organization 
also includes Pocket Ark which is the upcoming private server for Mass Effect Andromeda

## 🤳🏻 Discord Server

The Pocket Relay/Ark projects make use of a Discord server for help, suggestions, and development updates. 
Join it below to stay updated:

[Discord Server (discord.gg/yvycWW8RgR)](https://discord.gg/yvycWW8RgR)


## 👏🏻 Supporting these projects

These projects are free and open source, because of this I don't make any money from them. If you like these projects
and would like to support future development consider becoming a sponsor or donating below:

[GitHub Sponsors](https://github.com/sponsors/jacobtread)

<a href="https://www.buymeacoffee.com/jacobtread" target="_blank"><img src="https://github.com/jacobtread/jacobtread/blob/main/bmc-button.png?raw=true" alt="Buy Me A Coffee" height="41" width="174"></a>

## 📌 EA / BioWare Notice
The Pocket Relay software in all its forms are in no way or form supported, endorsed, or provided by BioWare or Electronic Arts.

## Instructions

For instructions on creating or connecting to a server see the guides on the **Pocket Relay** website 
[Guides](https://pocket-relay.pages.dev/guide/)

## Projects

### Server (https://github.com/PocketRelay/Server)

This repository contains the code for the server portion of **Pocket Relay**. This is the server
that clients connect to in order to play the game

### Client (https://github.com/PocketRelay/Client)

The client application which configures client computers to be able to connect to
**Pocket Relay** servers rather than the official servers.

### Embedded Client (https://github.com/PocketRelay/EmbeddedClient)

This repository contains the code for a new _experimental_ type of **Pocket Relay** client
that directly hooks into the games host resolution. This removes the need for the client to
require admin permissions and access the hosts file.

> This version is still experimental and may be incompatible with some mods or versions of the game

### Dashboard (https://github.com/PocketRelay/Dashboard)

This repository contains the source code for the dashboard that **Pocket Relay** uses

### Pocket Ark Server (https://github.com/PocketRelay/PocketArk)

This repository contains the code for the server portion of **Pocket Ark**. This is the server
that clients connect to in order to play the game

### Pocket Ark Client (https://github.com/PocketRelay/PocketArkClient)

The client application which configures client computers to be able to connect to
**Pocket Ark** servers rather than the official servers.

### Pocket Ark Hooks (https://github.com/PocketRelay/PocketArkHooks)

Hooking DLL to patch Mass Effect Andromeda and provide support for **Pocket Ark** servers

### Blaze SSL Async (https://github.com/jacobtread/blaze-ssl-async)

This is a custom implementation of the legacy SSLv3 protocol along with the 
TLS_RSA_WITH_RC4_128_SHA and TLS_RSA_WITH_RC4_128_MD5 cipher suites in order to 
support the required connections for gosredirector.ea.com. Common issue facing previous versions was finding support for this protocol and ciphers as due to how old it is most implementations require hacky solutions in order to enable it but this implementation is a pure rust implementation.

### Blaze SSL (https://github.com/jacobtread/blaze-ssl)

This is the syncronous version of Blaze SSL Async and is no longer maintained as its been superseeded by the async version

### BlazePK (https://github.com/jacobtread/BlazePK-rs)

This is a library which implements the Blaze packet system which Mass Effect 3 uses. This library
implements it in the Rust language. This library takes a encoding and decoding from structures 
approach when encoding packets. Through many improvements this library now also includes a packet routing system for routing
packets to functions

### BlazeKT (https://github.com/jacobtread/BlazeKt)

This is a library which implements the Blaze packet system which Mass Effect 3 uses. This library
implements it in the Kotlin language. This library takes a DSL / Typesafe builder approach when 
encoding packets

### Archived Manager (https://github.com/PocketRelay/PocketRelayManager)

This repository previously contained the management tool used to manage players and games on 
the server. It has since been archived and replaced by the dashboard interface which is now
built into Pocket Relay.

### Archived Kotlin Server (https://github.com/PocketRelay/ServerKotlin)
This is the previous implementation of the Pocket Relay server before the current Rust server. This
server is written in Kotlin and requires a JVM to run and will no longer recieve updates.

### RedirectorClient  (https://github.com/PocketRelay/RedirectorClient )

Previous iteration of a attempt at a redirector client. It was previously abandoned as it wasn't seen as the right solution
but the idea of having the redirector on the client has since been used again after the port to the new HTTP Upgrade system

The original proof of concept for this was written in Kotlin and is archived here https://github.com/PocketRelay/ClientKotlin

