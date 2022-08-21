# Server-Nukkit-Termux
This is the documentation on how to run the Nukkit server on termux

## Requirements

You must have Android 10 or higher
Arm64-V8 is required on your phone

Next you have to install Termux. I recommend downloading Termux on F-Droid. Because [Termux Download](https://f-droid.org/packages/com.termux/) on ChPlay is no longer supported.

## Creating the Server

Launching the Termux application, we enter the following command:
`termux-setup-storage` And Choose "Allow"

##### install Ubuntu

Next, they will upgrade and install what is needed for Ubuntu Focal to work, enter the following command

`apt-get update && apt-get upgrade -y && apt-get install wget proot git -y`

After completing the installation as above. We will proceed to boot Ubuntu
Enter the command as follows:

`cd`

`git clone https://github.com/BeanGTA/Linux-Termux-Nukkit.git`

`cd Linux-Termux-Nukkit`

`bash ubuntu.sh -y`

`bash startubuntu.sh`

##### install server

So you have entered the world of Linux Ubuntu. Okay we will continue to install Java 8 and Nukkit

Enter the command as follows:

`apt-get update && apt-get upgrade && apt-get install wget openjdk-8-jdk -y`

Next download the server Nukkit For Ubuntu

Enter the command as follows:

`mkdir nukkit`

`cd nukkit`

`wget https://ci.opencollab.dev/job/NukkitX/job/Nukkit/job/master/lastSuccessfulBuild/artifact/target/nukkit-1.0-SNAPSHOT.jar`

And start and running Nukkit on Ubuntu

`java -jar nukkit-1.0-SNAPSHOT.jar`







## How do I modify my server?
How can I add a plugin or for example change the default texture pack of my server?, In this section I will explain how to do it

If the server is online you need to stop it, then type in the console `stop`

![Stop Server](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-22-38-50-03_84d3000e3f4017145260f7618db1d683.jpg)

You are now in the ubuntu machine, you will see this
`root@localhost:~#` Then type `exit` to exit the ubuntu machine

![Exit Ubuntu](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-22-39-45-97_84d3000e3f4017145260f7618db1d683.jpg)

Now execute this command
`cd ubuntu-fs/root/nukkit`

execute this command `ls` Here are the directories and files of the server, here you can add plugins or change the properties of the server etc

![server file](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-23-51-31-35_84d3000e3f4017145260f7618db1d683.jpg)

**Note:** While the machine ubuntu or server is running, you will not be able to access the Folder `Nukkit`To modify the `properties` or for example "add a texture pack of the server".

#### How do I modify the server.properties?
Do the command `ls` to see all directories and all files

![Server File](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-23-51-31-35_84d3000e3f4017145260f7618db1d683.jpg)

Execute this command:
`nano server.properties` To edit the file

![nano](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-23-04-15-28_84d3000e3f4017145260f7618db1d683.jpg)

To save do `crl + x` On the keyboard

##### how do i run the Nukkit server again?

after modifying the server to your liking, it's time to Turn your server back on

You are now located in this folder `~/.../root/nukkit`

then execute `cd..` 3 times

Now do `ls` make sure you stay in this position

![start Ubuntu](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-23-26-07-25_84d3000e3f4017145260f7618db1d683.jpg)

Now run this command to log into the ubuntu machine
`./startubuntu.sh`

in case `./ startubuntu` does not execute do`chmod u+x startubuntu.sh` And try again

Now run this command to get into the server folder
`cd nukkit`

![start Ubuntu](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-23-32-42-21_84d3000e3f4017145260f7618db1d683.jpg)


Now execute this command

`java -jar nukkit-1.0-SNAPSHOT.jar`

![Server started](https://raw.githubusercontent.com/apoorslime/termux/main/Screenshot_2022-08-15-23-43-17-20_84d3000e3f4017145260f7618db1d683.jpg)

And there you have it now you have your server back online and ready to use enjoy ;)


