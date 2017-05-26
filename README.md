# Form-N-Fun
Form ‘N’ Fun is an android maze game based on real time computer vision. The uniqueness of this game is that the user can draw his own mazes on a white paper with pen/pencil and play. The game detects the maze and user can play using the accelerometer. This android app uses contours algorithms in OpenCV to detect maze that is drawn on the paper. This app uses JBox2d engine for simulating the rigid bodies.

<b>Download APK</b>

Apk can be found in apk folder, download and install the apk.

<b>Build Instructions</b>

Download <b>OpenCV for Android</b> (I used OpenCV 3.0.0) from http://opencv.org/releases.html and extract the file. I extracted the file to C:\opencv\OpenCV-3.0-android-sdk (I am using Windows Machine)

Open the <b>local.properties</b> file and set <b>ndk.dir</b> to the path of Android NDK folder.

For example on Windows local.properties look like this.

<b>sdk.dir = C\:\\android_sdk</b>

<b>ndk.dir = C\:\\android_ndk</b>


Open the <b>Android.mk</b> file in <b>jni folder</b>, modify the <b>export OPENCV_PACKAGE_DIR</b> to extracted OpenCV Path

For example on Windows. 

<b>export OPENCV_PACKAGE_DIR = C:/opencv/OpenCV-3.0-android-sdk</b>

<b>Run the app</b> after making the above changes.

<b>Note:</b>

I build it for all the Devices but I tested it only on NEXUS 5X.

<b>APP_ABI := arm64-v8a armeabi armeabi-v7a mips mips64 x86 x86_64</b>

If you want to build the App for a <b>particular device</b> then modify <b>APP_ABI to device ABIs</b> in Application.mk in jni folder.

For example, to build App only for <b>Nexus 5x</b> then modify <b>APP_ABI</b> to <b>APP_ABI:=arm64-v8a</b> in Application.mk (NEXUS 5X has ARMv8 based CPU supports AArch64).

<b>APP_ABI := arm64-v8a</b>

