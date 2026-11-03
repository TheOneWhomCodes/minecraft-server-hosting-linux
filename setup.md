

# Setup

## Java setup, Vanilla

first check if you have java installed with

```
java -version
```
If this does not work then do this to install it:

```
sudo apt update
sudp apt install openjdk-21-jre
```

After you've installed java, create a directory in your home folder like this:
```
mkdir ~/MinecraftServer
```

Now we will download the .jar file to run the server.

you can find the link to the download here: https://www.minecraft.net/en-us/download/server
**NOTE:** this is a .jar file of the most recent version, so tweak the first command to get the correct version!
Example:
```
sudp apt install openjdk-17-jre
```
This will download java version 17, preferable for older versions of minecraft like 1.20.1


Now to run the actual server, you get the downloaded .jar file and put it in your MinecraftServer folder we made, like this,
```
mv ~/Downloads/server.jar ~/MinecraftServer
```
**CHANGE THE NAME OF SERVER.JAR IF DIFFERENT!**

Now we will go inside our MinecraftServer folder while also running the server, like this
```
cd ~/MinecraftServer
java -Xms2G -Xmx4G -jar server.jar nogui
```
The java command means as follows
- Xms2G: Use at minimum 2 gigabytes of ram
- Xmx4G: if more is needed use at most 4 gigs of ram in total
- jar: tell it we're loading a .jar file
- nogui: do not host a client for the server too, only host the server

## Java setup, Modded

Follow the same steps for vanilla up until the server.jar part, instead
decide on a modloader, for this case we will use Forge.

Go to forge's website and your desired version and install the "installer"

<img width="1381" height="686" alt="image" src="https://github.com/user-attachments/assets/5a38a5ae-8a84-4326-b684-609fef63a7c9" />

After you've installed it move the installer into your MinecraftServer folder, like this:
```
mv ~/Downloads/forge-bla-bla ~/MinecraftServer
```

after that run the installer like this

```
cd ~/MinecraftServer
java -jar forge-bla-bla --installServer
```

This will setup your server up until the eula, go inside the eula.txt and change it from false to true.
You can use nano to do this easily:
```
nano ~/MinecraftServer/eula.txt
```

if you don't see eula.txt yet, then use the run.sh command first like this
```
bash ~/MinecraftServer/run.sh
```
then run this command again after you changed the eula to true
and boom your setup is completed!

## Adding mods!

Go to your prismlauncher or curseforge or modrinth or whatever and download a mod!

Extract the .jar files and then transfer them to your MinecraftServer's mods folder, like this:
```
unzip ~/Downloads/modpack.zip  ~/MinecraftServer
```
**NOTE: This is just a guess on where your zip file is saved on your system, it could very bell be saved somewhere else!**
**NOTE: Make sure to ONLY include .jar files in your mods folder!**
