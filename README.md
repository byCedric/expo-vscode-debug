# Test debugging

This project demonstrates the new debugging functionality.

## How to run

Install the vscode "Expo Tools" version, from this repository by right clicking the `.vsix` file and select "Install".

After that, you have two methods to start the vscode debugger:

1. Execute the command: `Expo: Debug app on device`
2. Launch the `Debug app` task through "Run and Debug".

## Start bundler

The bundler is using unreleased functionality. To use the proper version:

- Check out `@bycedric/cli/experimental-inspector-proxy-vscode-compat` in **expo/expo**
- Go to **expo/expo** and run `$ cd packages/@expo/cli && yarn install`
- Go back to this repository
- `$ EXPO_USE_CUSTOM_INSPECTOR_PROXY=true expod start`

## Using dev client

You can also use a dev client.

- `$ yarn expo install expo-dev-client`
- `$ yarn expo run:ios` (or `run:android`)
- Wait until it's complete, close the bundler
- `$ EXPO_USE_CUSTOM_INSPECTOR_PROXY=true expod start --dev-client`
