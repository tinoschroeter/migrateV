## HOWTO migrate Virtual Server from one Hypervisor to another

### first of all

```
~ deploay or start a new Server with the same Linux System
~ login with root and change to runlevel 1 (init 1)
~ bring your network up ifup eth0||ens3
~ find your IP (ifconfig)
~ start your ssh daemon service ssh start
~ go to your old Server and follow the installation steps

```

### Install and Usage:

```
~ # on the Server you want to migrate (Bare Metal / VMWare / Xen / Hyper-V / what ever)
~ sudo wget -O /usr/local/bin/migrateV https://raw.githubusercontent.com/tinoschroeter/migrateV/master/migrateV
~ sudo chmod +x /usr/local/bin/migrateV
~ migrateV [IP Address of your new VM]
~ done

```

### if you have Databases or something similar on your machine !!STOP IT!! 
in the most cases it will work anyway...

```
        ####################                     =          ###############
        # original Server  #                       =        # new Server  #
        #                  #      ====================      #             #
        #   migrateV       #      ====================      #   init 1    #
        #                  #                       =        #  10.0.0.1   #
        ###################                      =          ###############
```

.center[screenshot](https://raw.githubusercontent.com/tinoschroeter/migrateV/master/fishbowl.jpg)
