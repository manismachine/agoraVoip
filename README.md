With this sample app, you can:

- Join / leave channel
- Mute / unmute audio
- Switch speaker

## Running the App
**First**, create a developer account at [Agora.io](https://dashboard.agora.io/signin/), and obtain an App ID. Note you can get a temp token from dashboard project page (Can be used to join given channel only). Update "app/src/main/res/values/strings.xml" with your App ID and Token.

```
<!-- PLEASE KEEP THIS App ID IN SAFE PLACE -->
<!-- Get your own App ID at https://dashboard.agora.io/ -->
<!-- After you entered the App ID, remove <##> outside of Your App ID -->
<!-- For formal released project, please use Security Keys/Token
    https://docs.agora.io/en/Video/token?platform=All%20Platforms -->
<string name="agora_app_id"><#YOUR APP ID#></string>
<!-- Please leave it if not enable App Certificate -->
<!-- You can generate a temporary token at https://dashboard.agora.io/projects -->
<string name="agora_access_token">#YOUR ACCESS TOKEN#</string>
```

**Next**, integrate the Agora Voice SDK and there are two ways to integrate:

- The recommended way to integrate:

Add the address which can integrate the Agora Voice SDK automatically through JCenter in the property of the dependence of the "app/build.gradle":

```
implementation 'io.agora.rtc:voice-sdk:3.0.0'
```
(Adding the link address is the most important step if you want to integrate the Agora Video SDK in your own application.)
- Alternative way to integrate:

First, download the **Agora Voice SDK** from [Agora.io SDK](https://www.agora.io/en/download/). Unzip the downloaded SDK package and copy ***.jar** under **libs** to **app/libs**, **arm64-v8a**/**x86**/**armeabi-v7a** under **libs** to **app/src/main/jniLibs**.

Then, add the fllowing code in the property of the dependence of the "app/build.gradle":

```
compile fileTree(dir: 'libs', include: ['*.jar'])
```

**Finally**, open project with Android Studio, connect your Android device, build and run.

Or use `Gradle` to build and run.

## Developer Environment Requirements
- Android Studio 3.0 or above
- Real devices (Nexus 5X or other devices)
- Some simulators are function missing or have performance issue, so real device is the best choice

