# Server-Nukkit-Termux
This is the documentation on how to run the Nukkit server on termux

## Requirements

You must have Android 10 or higher
Arm64-V8 is required on your phone

Next you have to install Termux. I recommend downloading Termux on F-Droid. Because [Termux Download](https://f-droid.org/packages/com.termux/) on ChPlay is no longer supported.

## Creating the Server

Launching the Termux application, we enter the following command:
`termux-setup-storage` And Choose "Allow"

Next, they will upgrade and install what is needed for Ubuntu Focal to work, enter the following command

`apt-get update && apt-get upgrade -y && apt-get install wget proot git -y`

After completing the installation as above. We will proceed to boot Ubuntu
Enter the command as follows:

`mkdir nukkit`

`cd nukkit`

`wget https://ci.opencollab.dev/job/NukkitX/job/Nukkit/job/master/lastSuccessfulBuild/artifact/target/nukkit-1.0-SNAPSHOT.jar`

command to execute Nukkit:
`java -jar nukkit-1.0-SNAPSHOT.jar`

## How do I modify my server?
How can I add a plugin or for example change the default texture pack of my server?, In this section I will explain how to do it

If the server is online you need to stop it, then type in the console `stop`

![Stop Server]()

You are now in the ubuntu machine, you will see this
`root@localhost:~#` Then type exit to exit the ubuntu machine

Now execute this command
`cd ubuntu-fs/root/nukkit`

execute this command `ls` Here are the directories and files of the server, here you can add plugins or change the properties of the server etc

**Note:** While the machine ubuntu or server is running, you will not be able to access the Folder `Nukkit`To modify the properties or for example "add a texture pack of the server".

##### How do I modify the server.properties?
Do the command `ls` to see all directories and all files

Execute this command:
`nano server.properties` To edit the file

To save do `crl + x` On the keyboard

##### how do i run the Nukkit server again?

You are now located in this folder `~/.../root/nukkit`

then execute `cd..` 3 times

Now run this command to log into the ubuntu machine
`./startubuntu.sh`

Now run this command to get into the server folder
`cd nukkit`

Now execute this command

`java -jar nukkit-1.0-SNAPSHOT.jar`

![hy]()

https://f.cloud.github.com
