# Using arduino-cli with the Arduino Uno

## Installation
To start follow these steps:
[arduino-cli Installation](https://arduino.github.io/arduino-cli/0.35/installation/)
```bash
# Need to use zsh shell, fish shell seems to hate arduino-cli
chsh -s /bin/zsh
brew update
brew install arduino-cli
arduino-cli version
arduino-cli  Version: 0.35.2 Commit: 01de174c Date: 2024-01-24T11:12:30Z

arduino-cli config init
Config file written to: /Users/lkoepsel/Library/Arduino15/arduino-cli.yaml

arduino-cli core update-index

# plug-in arduino uno
arduino-cli board listall
arduino-cli core install 

```

## Overall Process
For each sketch, add a folder with the ino file as well as a makefile. There is an example for blink. When you want to compile and upload, run `make`, it will compile if required and upload the hex file to the Uno.

### Environment Variables
You will need to set the environment to match your own:

```bash
BOARD=arduino:avr:uno
PORT=/dev/cu.usbmodem4101
BUILD=build
```