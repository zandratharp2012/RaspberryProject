Exploring Hardware
##################

Board History
*************	

The Raspberry Pi was created in 2012 that was founded in 2009 by a charity organization called The Raspberry Pi Foundation located in the UK. Its founders were Eben Upton, David Braben, Alan Mycroft, Rob Mullins, Pete Lomas, and Jack Lang. With its intent in promoting Computer Science and fundamentals of computing, the raspberry pi was followed by the “Dyna-Micro”, or the “MMD-1” that was built in 1976.

The Story 
The Raspberry Pi was initially designed for learning purposes because it was cost efficient, yet powerful. Its intentions was built for the main purpose to educate kids and bring back the interest in showing how computers work. A breakable computer played an important factor in creating the device, which is why, the credit card sized board was designed for portability. 
Eben Upton was influenced with this idea when he was a Director of Studies in Cambridge. He recalled at a bonfire party in 2007, an eleven year old boy told him he wanted to be an electrical engineer and expressed his disappointment at realizing the boy did not have access to a  computer he could program on. Eben stated, “I said, ‘Oh, what computer do you have?’ and he says, ‘I have a Nintendo Wii.’ And there was just that awful feeling about there being a kid who was excited, a kid showing a concrete interest in our profession, but did not have access to a programmable computer of any sort. He just had a game console.”
He also noticed only a few student applications have applied in studying computer science and a significant number of applications in CS had dropped from 600 to 250. Upon research, it wasn’t the lack of teachers, it was more about the disinterest in the subject. Home computers in the 1980’s that were easily programmable back then, were no longer available in the 1990’s. Eben stated in his interview with TechCrunch UK,  that “...the supply of kids who would learn to program, also went away. We wake up 10 years later, and we’ve got no one applying to our computer science courses.”

The Models:
It initially released 2 model devices, the Model A and Model B (most common). The difference between the two models is the Model has 1 USB port and no ethernet port, whereas the Model B has 2 USB ports along with an ethernet port. 
 Although the Model B is the one most commonly available, the foundation’s aim is to sell the Model A at a lower cost for $25. Apart from the cost pricing difference, the power supply of the Model A offers an advantage of providing less power and can be powered by 500 mA supplies (general power battery adapters, battery packs, etc). Another enhancing feature for the Model A is the memory space that was originally built with 128 of RAM, will have 256MB, as will the Model B shipping with 512 MB selling for the current price $35)


Basic Board Setup
*****************

    * Power cable
    * Raspberry Pi
    * External Display 
    * External Display Connector
    * SD Card
    * External Mouse
    * External Keyboard

Development Tools
*****************

There are a few development tools that you will need in order to get an operating system working on a Raspberry Pi. There are many options when it comes to Gnu Compilers such as Java, Fortran, and Libc6 but we decided to use C/C++ Compiler.

Program Build Tools
===================

Command Line
------------
The command line will be used to download, extract the docker image, flash the SD card as well as locating an IP address for your machine and Raspberry Pi. Once the Raspberry Pi is operating, you can access it remotely using the command line and give it instructions. 

Gnu C++ Compiler
----------------
gcc is a compiler you can install and the one we chose to install on the Raspberry Pi. There are others offered such as the ones mentioned above (Java, Fortran, Libc6).

Docker
------
Docker simplifies the packaging, distribution, installation and execution of complex applications. We installed a few containers consisting of Ubuntu, redis(open source key-value store that functions as a data structure server), debian(Linux distribution that's composed entirely of free and open-source software) ,and hello-world(minimal image). 


..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/Docker.PNG
    :scale: 50%
    :align: center 


7-Zip
-----
This tool is used on a Windows machine in order to extract files and move files to the SD card containing the docker image.

Win32 Disk Imager
-----------------
This tool is used on a Windows machine and is needed to flash the SD card with the docker image. 
 

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/Win32.PNG
    :scale: 50%
    :align: center 


Putty
-----
This tool is used on a Windows machine and is an open-source terminal emulator, serial console and network file transfer application. It assists with establishing a connection to the Raspberry Pi

Zenmap
------
This tool is used in order to identify the IP address of your Raspberry Pi. 
 

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/Zenmap.PNG
    :scale: 50%
    :align: center 


Once your machine is up and running you can give it a cool command so it displays a hello message!


..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/HelloWorld.PNG
    :scale: 50%
    :align: center


..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/EchoHelloWorld.PNG
    :scale: 50%
    :align: center  


Processor Architecture
**********************

The Raspberry Pi has a Broadcom BCM2837 SoC (system-on-chip) with 4 ARM Cortex-A53 cores. Each processing core runs at 1.2Ghz with 32kB Level 1 and 512kB Level 2 cache memory, it also has a VideoCore IV graphics processor running at 400MHz. The Cortex-A53 processor is a high efficiency processor that implements the Armv8-A architecture. Armv8 supports 64-bit data processing, extended virtual addressing and a 64-bit general purpose registers. The Cortex-A53 processor has the following configuration.

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/A53Configuration.png
    :scale: 50%
    :align: center 

Processor Assembly Language
*************************** 

ARM is a family of instruction set architectures for computer processors and is used by the processor of the Raspberry Pi. Arm makes 32-bit and 64-bit RSC multi-core processors. The features of the ARM processor is as following:

    * Load/store architecture
    * An orthogonal instruction set 
    * Mostly single-cycle execution
    * Enhanced power-saving design
    * 64 and 32-bit execution states for scalable high performance
    * Hardware virtualization support

Below is an image of the ARM format summary and instruction set in more detail.

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/Formatsummary.PNG
    :scale: 50%
    :align: center


..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/InstructionARM.PNG
    :scale: 50%
    :align: center

Demonstration Project
*********************

There are two different ways we explored to set up the Raspberry Pi. Using the Mac, we set up the Raspberry Pi from the command line installing Docker first. This allowed us to work solely from the command line the entire process. Using Windows, we set up the Raspberry Pi with Raspbian first, then installed Docker, and used the built-in VNC Server/Viewer software to visually access the Raspberry Pi from a remote location. 


Mac Process:

You can use the following link to assist with the process in getting your system working:

    * https://blog.hypriot.com/getting-started-with-docker-and-mac-on-the-raspberry-pi/

First we need to download the Docker image from the website below. 

    * https://blog.hypriot.com/downloads/

Once the download has completed, you can use terminal to extract the zip file using "unzip Hypriot-rpi-201???.img.zip." Once the download has completed, you can flash your SD card using something like the following command in terminal:

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/FlashSD.PNG
    :scale: 50%
    :align: center

You will then boot the Raspberry Pi connecting it with power, SD card inserted, HDMI to external display hooked up and ethernet cable connected. Once Docker is running we need to be able to access it remotely. Locating your IP address is necessary so we are able to find that with typing in "ifconfig getifaddre en1" or using en0 if connected by ethernet to your machine. Once your IP is located, you can use Nmap in terminal in order to locate the IP address of your raspberry pi. If the command is not recognized in terminal and your system does not have Nmap installed, you can download the package installer at nmap.org for MacOS X installer or use Home-brew to install from the command line on your machine. Once you know Nmap is working, using the following command, "nmap -sP <yourIPaddressgoeshere>/24 | grep black-pearl", will allow you to locate the IP address of your Raspberry Pi. Once you find it, you can type in "ssh pirate@<RasbperryPiIPAddressgoeshere>" and it will ask you to enter a password which is "Hypriot". You will enter "yes" when asked if you are sure you want to connect to the Raspberry Pi. To check if everything worked as it should have, type in the command "docker info" and you should see information about the containers and other items. It should look similar to the image below.

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/Dockerinfo.PNG
    :scale: 50%
    :align: center

You are ready to install an image using Docker and you can do something really cool like run a program all within the command line. I installed different images on such as Ubuntu, Debian, Redis. You can browse a selection of images ready to install on the Docker Hub.

    * https://hub.docker.com

Once you choose the one desired, using your machine to access Raspberry Pi remotely, you can enter a command such as "docker run ubuntu." Let's say you wanted to run a program such as "Hello-World" also located in the Docker Hub. You can pull it using "docker pull hello-horld" and ask Docker to run it. It would look something like the following image:

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/HelloWorld.PNG
    :scale: 50%
    :align: center

Windows Process:

For the Windows process we first installed NOOBS(New Out Of Box Software) onto the SD card. NOOBS is an operating system installation manager that makes it easy to install operating systems on the Raspberry Pi. You can download NOOBS from the following link:

    * https://www.raspberrypi.org/downloads/noobs/

Once you have NOOBS on the SD card, insert it into the Raspberry Pi and boot it up. You should see a screen like this:

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/noobs.png
    :scale: 50%
    :align: center

On this screen you can select the Raspbian OS to install or you can connect to the internet via WiFi or ethernet and get a list of different operating systems to install. The installation process takes quit some time for Raspbian so be patient! Once the installation is complete you will be prompted to reboot the Pi. After the reboot, Raspbian starts and you should see a screen similar to the image below: 

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/raspbianstretch.png
    :scale: 50%
    :align: center

Raspbian has a built in tool called RealVNC that allows you to connect remotely. You need to enable the built in VNC server on the pi and you will also need to download VNC viewer onto the machine you will be using to connect remotely. RealVNC is available for download at the following link:

    * https://www.realvnc.com/en/

After setting up and connecting VNC, you can disconnect the monitor and keyboard and control the Pi remotely.  

Now we installed Docker using the terminal by typing in the following command:

..  image:: https://github.com/zandratharp2012/blob/master/raspberryproject/presentation_images/dockercmd.png
    :scale: 50%
    :align: center

