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

Below are links and descriptions of associated projects

- [Pocket Relay Server](https://github.com/PocketRelay/Server)
  - This repository contains the code for the server portion of **Pocket Relay**. This is the server that clients connect to in order to play the game
- [Pocket Relay Client](https://github.com/PocketRelay/Client)
  - The client application which configures client computers to be able to connect to **Pocket Relay** servers rather than the official servers.
- [Pocket Relay Embedded Client](https://github.com/PocketRelay/EmbeddedClient)
  - This repository contains the code for a new _experimental_ type of **Pocket Relay** client that directly hooks into the games host resolution. This removes the need for the client to require admin permissions and access the hosts file.
  - > **Warning**
    > This version is still experimental and may be incompatible with some mods or versions of the game
- [Pocket Relay Dashboard](https://github.com/PocketRelay/Dashboard)
  - This repository contains the source code for the dashboard that **Pocket Relay** uses
- [Pocket Ark Server](https://github.com/PocketRelay/PocketArk)
  - This repository contains the code for the server portion of **Pocket Ark**. This is the server that clients connect to in order to play the game
- [Pocket Ark Client](https://github.com/PocketRelay/PocketArkClient)
  - The client application which configures client computers to be able to connect to **Pocket Ark** servers rather than the official servers.
- [Pocket Ark Hooks](https://github.com/PocketRelay/PocketArkHooks)
  - Hooking DLL to patch Mass Effect Andromeda and provide support for **Pocket Ark** servers
- [Blaze SSL Async](https://github.com/jacobtread/blaze-ssl-async)
  - This is a minimal Rust implementation of the SSLv3 protocol specifically to support connections from the Mass Effect 3 client this is used by the client tool in order to handle trafic without requiring on hacky system tweaks or large C libraries.
  - The previous syncronous version of this is no longer maintained but is still visible at https://github.com/jacobtread/blaze-ssl
- [BlazePK](https://github.com/jacobtread/BlazePK-rs)
  - Library which provides encoding, decoding, framing, and routing support for the packets that ME3 uses


## Archived Projects

Below are projects that were previously used for this but have since been archived/deprecated

- [BlazeKT](https://github.com/jacobtread/BlazeKt)
  - Library which provided encoding and decoding support for ME3 packets back for the old Kotlin server (No longer maintained)
- [Pocket Relay Manager](https://github.com/PocketRelay/PocketRelayManager)
  - This repository previously contained the management tool used to manage players and games on the server. It has since been archived and replaced by the dashboard interface which is now built into Pocket Relay.
- [Kotlin Server](https://github.com/PocketRelay/ServerKotlin)
  - The original server implementation that was written in Kotlin
- [Redirector Client](https://github.com/PocketRelay/RedirectorClient)
  - Previous iteration of a attempt at a redirector client. It was previously abandoned as it wasn't seen as the right solution but the idea of having the redirector on the client has since been used again after the port to the new HTTP Upgrade system
  - The original proof of concept for this was written in Kotlin and is archived here https://github.com/PocketRelay/ClientKotlin

