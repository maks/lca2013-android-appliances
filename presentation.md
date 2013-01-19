Building Appliances with Android
    
    welcome to the presentation. 
    I am going to talk about building appliances with android.
    
Or how to turn a droid into a toaster

    subtitle

Appliances

    I'm talking about apps designed to take over the device, to be the sole focus of the device.
     
What do I mean by Appliances?

    So what do I mean by appliances?

<pre>
ap·pli·ance  
/əˈplīəns/
Noun

    A device designed to perform a specific task, 
    typically a domestic one.
</pre>

    Well the dictionary says...

![Images](images.png)

    And I mean things like this
    
![Images](images.png)

    And this
    
![Images](images.png)

    And this. 

Customisation

    Now in order to create an appliance using Android you need to be able
    to customise it.

3 Levels 
    
    And with Android you pretty much have 3 levels in which to work at
        
1 User

    By User-level I'm talking about using the normal means that a normal app
    developer or regular device user has at their disposal

2 Root

    This is just what it says. The main thing to note here is that with Android devices,
    as with most other phone device OS's, is that unlike with laptops and desktops,
    the end user does not normally have nor is **intended** to have root access to the device.
    Of course anyone working in a corporate environment would already be used to this
    state of affairs but unfortunatly it is now spreading widely in the consumer space.

3 OS

   This is the lowest or deepest level of customisation, where you are infact rebuilding
   the whole operating system from the source, yes wave hello to any Gentoo users out there!
   
   
User Level Customisation

Things you can do...

    So what can you do at this level?

Use the Home Intent

    Well you can use the home intent. 
    
Small Detour - What are Intents?

    But for those that arent Android app devs, what is an Intent? Basically they
    are an IPC mechanism, similar to DBUS. Android is actually really made up of 
    a suite of co-operating components, bundled sometimes as applications 
    communicating through direct and broadcast messages called Intents.

Use "public API" Intents (eg. Wifi config)
    
    Use "public API" Intents for example Wifi configuration (show demo)

## Root Level

Things you can do:

* access protected APIs (eg. reboot)
* **SILENT** OTA updates of your apps


Actually a Trilogy in 4 parts

* User
* Root
* OS -> __Android Framework__
* OS -> __Kernel__

    So actually I lied, theres really 2 parts to the OS-level customisation,
    customisation at the Android Framework layer and below that at the Linux
    kernel layer.

AOSP and Building Android

* hundreds of git repos
* huge amounts of disk space req'd
* min 1hr on a __very__ **fast** machine !
* ...and then you need to build img & test on emu/device :-(
    
    So building android is fairly straight forward but you have to keep in mind
    you are essentially building a whole linux distrubtion from source.

OS - Android

Things you can do:
* choose which apps to ship
* customise UI (eg. remove Systembar in ICS onwards)
* choose CPU platform (eg. x86 instead of ARM)
* workaround bugs in hardware (eg. bad LCD EDID)
* **control** the platform - use __your own__ signing certs

    Once you get to this level, you have a whole lot of control. You can

OS - Kernel

* device drivers, eg. non-HID touchscreens

    This is just liek building a custom kernel for your favourite desktop distro.
    The reasons you would do this are the same, such as adding support for an
    unusual piece of hardware like a non-HID touchscreen for example.

Thank You! 

* blog.manichord.com
* maks@manichord.com
* github.com/maks
* @mklin

    Thank you - any questions