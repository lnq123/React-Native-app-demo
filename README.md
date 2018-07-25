# React Native - Coding challenge?

src = https://github.com/Unity-Labs-Development/React-Native-app-demo



Problem:
---------

1. After entered two pin code, it crushed by the prop `currentBalance` is marked as required in `BalanceRow`, but its value is `undefined`.

2. When Change pin code, it wont return to home page if the code is corrent.
eg. Enter 1234, ask for repeat the code. Then enter 1234(meanwhile it stores new code as 1234). However, on phone screen user only could keep typing as 123456789 or press return button.


3. cant add new coin

How to fixed
------------

1. In src/screens/WalletHome/index.js:179
Reset if currentBalance is undefined, or keep the value.
After fixed, we could log to the WalletHome page.

2. In src/screens/CreateWallet/index.js:119
There is not page called Wallet. Change it to WalletHome to fix.

3. Somehow user add token new coin didnt store to redux store and cant show in home page.


## Local development

Make sure you have `react-native-cli` installed.

```bash
# Install dependencies
$ npm install

# Run project on connected iPhone or iOS simulator
$ react-native run-ios

# Run project on connected iOS simulator as Iphone 8
$ react-native run-ios --simulator="iPhone 8"

# Run project on connected Android device or running Android simulator
$ react-native run-android
```