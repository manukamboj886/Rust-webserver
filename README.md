Rust-webserver
Setting up Rust on Fedora
This guide will walk you through the process of setting up Rust programming language on Fedora.

Step 1: Install Rust
Open a terminal window.
Update your package index:
console



$ sudo dnf update
Install Rust using rustup, which is the official Rust installer:
console



$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
Follow the prompts to complete the installation.
Once the installation is complete, you'll be prompted to run the following command to add Rust to your system PATH:
console



$ source $HOME/.cargo/env
Step 2: Verify Rust Installation
To verify that Rust has been installed correctly, you can run:
console



$ rustc --version
You can also check the version of Cargo, the Rust package manager, by running:
console



$ cargo --version
Step 3: Update Rust and Cargo
To keep Rust and Cargo up to date, you can use rustup:

console



$ rustup update
Installing Dependencies for Rust Projects on Fedora
This guide will walk you through the process of installing dependencies for your Rust projects on Fedora using Cargo, the Rust package manager.

Adding Dependencies to Cargo.toml
Before installing dependencies, you need to specify them in your project's Cargo.toml file. Open the Cargo.toml file located in your project's root directory and add your dependencies under the [dependencies] section. For example:

toml



[
dependencies
]
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
This adds two dependencies: serde and serde_json.

Using Cargo to Install Dependencies
Once you've specified your dependencies in the Cargo.toml file, navigate to your project directory in the terminal and run the following command to install them:

console



$ cargo build
This command will fetch and build all the dependencies listed in your Cargo.toml file. If you only want to download the dependencies without building your project, you can use:

console



$ cargo fetch
Checking Dependencies
After running the appropriate cargo command, Cargo will download and install the specified dependencies. You can verify that the dependencies are installed correctly by checking the Cargo.lock file and the target directory in your project's root directory.

Running the Web Server
To run the web server, use the following command:

console



$ cargo run --package http-server --bin http-server 127.0.0.1:5666
Additional Resources
Rust Programming Language Official Website
Rust Documentation
Rust By Example
The Cargo Book (Cargo Guide)
Rust Cookbook
