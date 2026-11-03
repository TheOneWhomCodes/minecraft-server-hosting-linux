

# Setup

## Java setup!

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
  
