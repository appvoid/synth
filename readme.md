# Synth

![synth_project](https://user-images.githubusercontent.com/78444142/161784980-0322cc73-26c1-4f5c-9eff-34ac5667782f.png)

SynthMotion (or just Synth) is an appimage tool that let's you build appimages for Linux super easy. Just need to locate your app and you are ready to go.

***
### 📝 **Quick install**
No needed, since it is an AppImge it works on virtually any distro! So you just need to type:

``sudo apt-get install python3-pil python3-pil.imagetk && git clone https://github.com/appvoid/synth.git && ./synth/synth.dist/synth.AppImage``
***
### 📝 **Requirements**

- 🐧 Linux
- 📄 Executable file
- 🎴 PNG icon file

Even though is super easy to create them, there are some things you need to consider when creating or porting your existing app to a SynthMotion app. You should have an executable file and an icon.png. Your app should contain an icon.png next to your executable, for example, you should have an structure like this:

app | icon.png

This is the bare minimum to make SynthMotion to compile your app into an appimage.

**Note**

If your app uses local resources, which is pretty common, you should be providing to your app the base directory path where your app is located when mounted, like this:

``$APPDIR/usr/bin/``

For example, in a Python app, you should get the path of the project first and then use it to load your app's resources. Here's a simple way to achieve that:

``src_dir = os.popen("echo $APPDIR/usr/bin/").read().rstrip()``

Now we can use assets from within the AppImage:

``icon_path = src_dir+"icon.png"``

***

### **CLI** 💻
There is a CLI version which is actually the main version. Essentially, this tool was designed to autoreplicate itself into an app version that replicates AppImages for your executables, but can also be used to make AppImages, actually, it's the only way to (not manually) set a category for the app.
****
### **Usage (CLI)** 🚩
**DEV NOTE**: Things are still changing so expect breaking changes from different versions!

``* means is optional``

``./synth-cli compile <path-to-executable> <name*> <category*> ``

****
### ☕ **Donations and Support** 
Buy me a coffee! Creating this kind of things is tedious sometimes and enjoyable also. When you support a developer, you really make it to work a lot happier 😄
### [ 👉 **Donate using PayPal** ](https://www.paypal.com/donate/?hosted_button_id=CDZH8GJET9SNU)
### [ 👉 **Become a Patreon!** ](https://www.patreon.com/bePatron?u=52880328)

You can also spread the word! Share it with your nerd pals! Help fixing bugs! There is a lot you can do if you really wanna help me to create the most beautiful, simple and efficient way to create apps for Linux.

****
## Apps
If you make an app with this tool, please let us know!


## Contribuitors
#### **Thanks to FreePik from FlatIcon**
For that amazing default icon for the app template.
https://www.flaticon.com/free-icons/illustration

#### **Really BIG thanks to DT from YouTube!**
For that amazing tutorial on AppImages, without him, this app wouldnt have existed! https://www.youtube.com/watch?v=Wy63jwjpNg4
****
## Support and Troubleshooting
If you need better answers, chat with me here:
nohakcoffee@gmail.com
Remember to use the topic for subject "appvoid open source + your actual subject"

If an error related to FUSE appears, make sure to have installed FUSE:
`sudo apt-get install fuse libfuse2`

If it's still not working, check if the appimage is the actual architecture of your device.
