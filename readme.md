# Synth

### Tool for building appimages super easy!

SynthMotion (or just Synth) is an appimage tool that let's you build appimages super easy. Just need to locate your app and done!

### Requirements

Even though is super easy to create them, there are some things you need to consider when creating or porting your existing app to a SynthMotion app. You should have an executable file and an icon.png. Your app should contain an icon.png next to your executable, for example, you should have an structure like this:

app
icon.png

This is the bare minimum to make SynthMotion to compile your app into an appimage.

**Note** that if your app uses local resources, which is pretty common, you should be providing to your app the base directory path where your app is located when mounted, like this:

``$APPDIR/usr/bin/``

### Big thanks to FreePik from FlatIcon
For that amazing default icon for the app template.
https://www.flaticon.com/free-icons/illustration