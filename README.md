# Rust-webserver

# Setting up Rust on Fedora

This guide will walk you through the process of setting up Rust programming language on Fedora.

## Step 1: Install Rust

1. Open a terminal window.

2. Update your package index:


sudo dnf update


3. Install Rust using `rustup`, which is the official Rust installer:

Follow the prompts to complete the installation.

4. Once the installation is complete, you'll be prompted to run the following command to add Rust to your system PATH:

source $HOME/.cargo/env


## Step 2: Verify Rust Installation
```toml
[dependencies]
regex = "1"
http = "0.2.3"
mime = "0.3"
bcrypt = "0.15.1"
actix-web = "4.4"
serde = { version = "1.0", features = ["derive"] }
serde_json = "1.0"
bytestring = "1.2.0"
actix = "0.13"
actix-web-actors = "4.1"
actix-files = "0.6"
log = "0.4"
env_logger = "0.9"
mime_guess = "2.0.4"
percent-encoding = "2.2.0"
lazy_static = "1.4.0"

This will adds two dependencies: serde and serde_json.


Using Cargo to Install Dependencies
Once you've specified your dependencies in the Cargo.toml file, navigate to your project directory in the terminal and run the following command to install them:

cargo build


This command will fetch and build all the dependencies listed in your Cargo.toml file. If you only want to download the dependencies without building your project, you can use:

cargo fetch

Checking Dependencies
After running the appropriate cargo command, Cargo will download and install the specified dependencies. You can verify that the dependencies are installed correctly by checking the Cargo.lock file and the target directory in your project's root directory.




1. To verify that Rust has been installed correctly, you can run:


rustc --version


2. You can also check the version of Cargo, the Rust package manager, by running:


cargo --version


## Step 3: Update Rust and Cargo

To keep Rust and Cargo up to date, you can use `rustup`:



rustup update


## Additional Resources

- [Rust Programming Language Official Website](https://www.rust-lang.org/)
- [Rust Documentation](https://doc.rust-lang.org/)
- [Rust By Example](https://doc.rust-lang.org/stable/rust-by-example/)
- [The Cargo Book (Cargo Guide)](https://doc.rust-lang.org/cargo/)
- [Rust Cookbook](https://rust-lang-nursery.github.io/rust-cookbook/)

Install Dependencies:

# Installing Dependencies for Rust Projects on Fedora

This guide will walk you through the process of installing dependencies for your Rust projects on Fedora using Cargo, the Rust package manager.

## Adding Dependencies to `Cargo.toml`

Before installing dependencies, you need to specify them in your project's `Cargo.toml` file. Open the `Cargo.toml` file located in your project's root directory and add your dependencies under the `[dependencies]` section. For example:

```toml
[dependencies]
serde = "1.0"
serde_json = "1.0"


Runnig code ->>





