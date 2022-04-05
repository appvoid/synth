# Synth

### Tool for building appimages super easy!

![synth_project](https://user-images.githubusercontent.com/78444142/161784980-0322cc73-26c1-4f5c-9eff-34ac5667782f.png)

SynthMotion (or just Synth) is an appimage tool that let's you build appimages for Linux 🐧 super easy. Just need to locate your app and done!

***
### Requirements

Even though is super easy to create them, there are some things you need to consider when creating or porting your existing app to a SynthMotion app. You should have an executable file and an icon.png. Your app should contain an icon.png next to your executable, for example, you should have an structure like this:

app | icon.png

This is the bare minimum to make SynthMotion to compile your app into an appimage.

**Note** that if your app uses local resources, which is pretty common, you should be providing to your app the base directory path where your app is located when mounted, like this:

``$APPDIR/usr/bin/``

For example, in a Python app, you should get the path of the project first and then use it to load your app's resources. Here's a simple way to achieve that:

``src_dir = os.popen("echo $APPDIR/usr/bin/").read().rstrip()``

Now we can use assets from within the AppImage:

``icon_path = src_dir+"icon.png"``

***

### CLI
There is a CLI version which is actually the main version. Essentially, this tool was designed to autoreplicate itself into an app version that replicates AppImages for your executables, but can also be used to make AppImages, actually, it's the only way to (not manually) set a category for the app.

## Contribuitors
#### Big thanks to FreePik from FlatIcon
For that amazing default icon for the app template.
https://www.flaticon.com/free-icons/illustration