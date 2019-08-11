
## What problem am I solving?
* Programming keyboard are very expensive/overpriced. a low cost divice that can convert normal keyboard into would lower the cost of programmable keyboard dramatically.

    for example: 

    [X-Keys XK-60](https://www.amazon.com.au/X-keys-Programmable-Keypads-Keyboards-XK-60/dp/B0092SGI0C) cost $362 with 60 keys 

    vs

    [common keyboard](https://www.officeworks.com.au/shop/officeworks/p/j-burrows-wired-keyboard-black-jbkb620kb) that cost < $10 and has 101 keys

* Programmable keyboard don't have a standard way of programming, this make it hard for user to share their productivity/workflow configurations with other users.

* Mapping dedicated key to to perform IoT/hardware actions provide alternate way to interact with IoT device and is faster than using an UI but it's costly because Keyboards often require a computer with operating system and driver to work, an computer capable of running OS increases the cost of deployment. 

 

## Solutions:
Design a hardware device that
* Sits between keyboards and the target computer 
* Can take input from (onboard key, connected keyboard, wifi, http, mqtt, time event, bluetooth)
* Can process / map key to any key/key sequence
* Can send output anywhere (other computer(s) as keyboard emulator, bluetooth style keyboard emulator, write to storage device for key logging, send http, mqtt to IoT device and servers)
* Can be used without a host computer

* additional/future plan:
  support sending lora, inferred, serial

  
## What will make this product stand out?
The short answer is `user experience` in `software`.

**User friendliness**

App store /package manager that allows user share develop more IoT integration and user to share their key map and settings.

The device is 100% plug and play, there are no driver to be installed.

**Designed for hacking**

To lower the skill requirement for development on this produce, Javascript(low.js) is used as the main programming language, this enable an average developer to write app/complex keymap for the product.

The device can be connected to WIFI or act as a WIFI hotspot and user can develope and upload program without additional software and driver.

By using the ESP32 (a popular hardware microcontroller), developer and user have a lot of online resouce and document to gain lower level access.


**Low cost, simple and roubust**

The component chosen with low cost, simplicity and quality in mind. 

**versatile**
Can acts as IoT controller, keyboard key remapper, keyboard lighting effect controller, Keylogger, Wireless key injector, keyboard/mouse only KVM.

## Specific use cases 
* Record and replay keystroke (UI automation method accessible to general users)
* Keyboard automation for platform that only support simple keyboard, such as smart TV, PC BIOS/UEFI.
* use as wireless keyboard and mouse only KVM. KVM is a device allow sharing one keyboard/monitor/mouse between multiple computers, it's mostly in server rooms/data centers where admins need a quick way to switch between servers. 
* use as an wireless keylogger/injector (pen test tool)
* Convert a bluetooth keyboard USB one (Most desktop computer does not have bluetooth, this allows desktop computer to use bluetooth keyboard)
* Convert USB keyboard to wireless one
* Connect and control IoT devices with dedicated key.
* 


## Hardware product overview:
 **Main board:**

* Has a few programmable key dedicated key for menu access
* Can be connected to one computer with USB
* Can be connected multiple keyboards
* Has a small OLED screen to display info/time
* Has customisable RGB,   


**Wireless key injector & capture:**
* A small device that can be connected to the main board through wirelessly and receive keys and commands from the main board.
* Can be used as a wireless key injector & logger (pen test tool)

## Target user:
* Productivity users;
* People that works with complex software suit (MS office, Adobe Photoshop, Adobe premiere, Programming IDE etc)
* PC(computer) gamers
* Reddit community /r/mechanicalkeyboard
* General user with that wish to use keyboard/mouse to control IoT device.
* General user that wish to use macro in locked down / hardware that they do not own.


## What was done during the Hackerthon period ?
* A software demo to demonstrate how macros can be used.
* Lots of research on choosing the best component / cost optimisation
* Ciruit schematic (mostly done)
* PCM board layout (mostly done)


## What about software key mapper?
I am aware of the software solution out there (namely AutoHotKey) that does key remapping, keyboard/mouse automation.
However, there are some disadvantages:
* require installation of software and cannot be used on locked down machine, generally not portable
* Window specific, (not work on Mac, does not work on Linux, smart fridge)
* Does not have RGB ?

## Why is it called project firestarter?
As with many hardware, it could literally start a fire. If I named it firestarter, then it would be assumed that it's a feature instead of a bug/flaw in the design.  

More importantly it represents the iterate/experiment/fail fast spirit.

     
## Hardware parts used:
* ESP32: main microcontroller for running low.js code
* CH554G: low cost MCU Keyboard capture device
* Nrf42: Wireless module to connect to wireless key injector
* Oled scree for displaying time simple UI
* Keys: for menu access and setting up device without keyboard or computer

## Estamate Cost (per board):

* less than $10 for the main board
* less that $5 for the wireless capture & inject board.

## Alternative name for the final product:
* Fire starter is the project name for my own reference. Alternate  products name are being consider. (suggestion welcome ;)  
* Keyboard dock
* Keyboard smartilizer
* Keyboard intercepter
* Keystroke router
* IO mapper Input/output mapper
* Keyboard Relay
* Keyboard manager
* Input transformer


## How I built it

**Tools and technologies used**
* EasyEDA : circuit and PCB design 
* MicroPython: 
* AutoHotKey: demo


## Challenges I ran into
* Managing time was a challange
* Choosing component, often there are lot of simlar components with similar specs from different Manufacturer
## Accomplishments that I'm proud of


## What I learned
* How to make a scanning key matrix:
Scanning 




## What's next for Firestarter
Oder PCB, write firmware, internal testing. 
Send sample to users and ask for feebacks.
Open source the platform.
Share it on keyboard / productivity forum
Sell assembled hardware.
