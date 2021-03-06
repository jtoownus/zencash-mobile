# ZENCash Mobile

ZENCash mobile app built using Onsen UI, Redux, React and Webpack.

Use node v6.15.1

## Setup instructions

```
export ANDROID_HOME=<path to sdk>
npm install -g yarn cordova@7.1.0
yarn install
cordova plugin add cordova-plugin-qrscanner cordova-plugin-file cordova-plugin-http cordova-clipboard cordova-plugin-inappbrowser cordova-plugin-device cordova-plugin-wkwebview-engine cordova-plugin-whitelist
cordova platform add android@6.2.3
cordova run android

# Generate a Signed APK
cordova build --release android
zipalign -v 4 <Example-release-unsigned.apk> <Example.apk>
apksigner sign --ks <keystorename> <Example.apk>

```

## Updating Color Scheme or Logo
Toolbar color scheme location:
```
assets/css/index.css
```

Logo location:
```
assets/img/zencash.png
```

### iOS FAQ

1. Icons

Icons are a bit of a pain to setup for iOS. Make sure you've added the ios platform to cordova, and copy the folder `./assets/img/ios/AppIcon.appiconset` to `./platforms/ios/ZEN\ Wallet/Images.xcassets`. Remove the folder `AppIcon.appiconset` if it exists in `./platforms/ios/ZEN\ Wallet/Images.xcassets`.

2. `.ipa` files (using it on a real iPhone)

```
1: Change scheme destination to Generic IOS device.

2: Click Product > Archive > once this is complete open up the Organiser and click the latest version.

3: Click on Export... option from right side of organiser window.

4: Select a method for export > Choose correct signing > Save to Destination.
```

2.1 Adding account to sign for the app

```
1. Xcode -> Preferences -> Account -> sign in with your apple id
2. https://i.stack.imgur.com/w4SlR.gif
```

# Contributors

[kendricktan](http://github.com/kendricktan/)

[alexanderzabuga](https://github.com/alexanderzabuga)

[kevinah95](https://github.com/kevinah95)

[afucher](https://github.com/afucher)

[andyvh](https://github.com/andyvh)

[darkavenger](https://github.com/darkavenger)

[emhaye](https://github.com/emhaye)

[simoneddeland](https://github.com/simoneddeland)

[dropnib](https://github.com/dropnib)

[rubyxroot](https://github.com/rubyxroot)

[berar](https://github.com/berar)
