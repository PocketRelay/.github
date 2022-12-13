# Manual Building

>This is a guide for manually building the server binary. 

## Requirements

- **Rust & Cargo** Rust version 1.65.0 or greater is required in order to compile the server
you can install both of these using Rustup which you can install using the guide [Here](https://www.rust-lang.org/learn/get-started)

- **Git** Git is required to clone the github repository to your system. You can ignore this step if you manually download the latest source archive from github directly [Here](https://github.com/PocketRelay/ServerRust/archive/refs/heads/master.zip). 

>If you are using the source zip directly then extract it to a folder and skip the "Clone Repository" step

## Crates.io

> NOTE This section is only for when the next stable release is published to crates.io until that happens attempting to install without specifiying the version flag (i.e. --version 0.1.2-alpha) will result in a broken hello world app installing instead

If you have Rust installed you can automatically download, compile, and install the server using the following command

```shell
cargo install pocket-relay
```

> When a new version is released you can use this same command to install the latest version

## Combined Answer

If you want skip all the steps and just have a list of commands to paste in for the default setup you can paste the following commands into to your terminal.

```shell
git clone --depth 1 https://github.com/PocketRelay/ServerRust.git pocket-relay
cd pocket-relay
cargo build --release
```

> Each line is its own command so copy them seperately

## 1) Clone Repository

First you need to clone the repository from Github using the git clone command. If you are doing this on the source archive directly you can skip this step

```shell
git clone --depth 1 https://github.com/PocketRelay/ServerRust.git pocket-relay
```

## 2) Move to the directory

In order to run the next commands you will need to have the pocket-relay folder as your current directory. If you are in the terminal you can use the following command

```shell
cd pocket-relay
```

## 3) Compile with Cargo

If you would like to build the server with just the default standard features use the following command

```shell
cargo build --release
```

If you would like to build the server with MySQL instead of using SQLite you can use the following command

```shell
cargo build --release --features database-mysql --no-default-features
```

> See the configuration guide for configuring the use of a MySQL database


## 4) Finding the executable

Once building is complete you will find the executable in `target/release` directory. If you are compiling on Windows the executable will be named `pocket-relay.exe` and if you are on linux it will be named `pocket-relay`

## 5) Done

Thats the end of the compiling guide refer back to the setup guide for instructions on running the executable