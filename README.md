# Octra_labs ocs01-test guide
A step-by-step guide to build and run octralabs ocs01 test. Works on windows, macos and linux

## Prerequisites
- Must have previously generated a wallet and Installed Octra_Pre_client CLI
- Follow this guide first if you haven't: https://github.com/0luwatunmise/Octra-Labs

- Install rust if not Installed, If installed skip
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```
## Confirm rust is installed
```
rustc --version
```

## Build the project from source
```
git clone https://github.com/octra-labs/ocs01-test.git
cd ocs01-test
cargo build --release
```

## Navigate to root directory and  move both the compiled binary and the execution interface JSON to your previously Installed Octra_Pre_Client CLI directory
```
cd
cp ./ocs01-test/target/release/ocs01-test ./ocs01-test/EI/exec_interface.json ~/octra_pre_client/
```

## Make the Binary Executable
```
chmod +x ~/octra_pre_client/ocs01-test
```

## Navigate to the CLI directory and run the binary
```
cd ~/octra_pre_client
./ocs01-test
```

After running, follow the menu to interact

## Credits
Original project: https://github.com/octra-labs/ocs01-test





