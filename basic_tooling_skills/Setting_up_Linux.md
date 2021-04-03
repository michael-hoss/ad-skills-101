## Setting up a Linux operating system

This content is adapted from [RWTH's Self-Driving Lab Wiki](https://git.rwth-aachen.de/ika/sdl1-ws2020/-/wikis/Exercises/Exercise-0-Prerequisites).

Perhaps the best way to get started is to install the latest [LTS](https://ubuntu.com/blog/what-is-an-ubuntu-lts-release) (long term support) version of Ubuntu, where Ubuntu is a so-called [Linux distribution](https://en.wikipedia.org/wiki/Linux_distribution).
Usually, Ubuntu LTS versions are released in even years ([Ubuntu 20.04](https://releases.ubuntu.com/20.04/), Ubuntu 18.04 etc.) and are supported with updates for five years.

:information_source: Note that ROS versions are often developed and tested with a certain Ubuntu version in mind, so if you want to use a specific ROS version, make sure to install the correct Ubuntu version for it.

You have two options to install a Linux distribution, coming from Windows or macOS:

1. **Dual boot:** Linux lives natively next to your existing operating system
    * plenty of installation tutorials are available, e.g., [this one](https://linuxconfig.org/how-to-install-ubuntu-20-04-alongside-windows-10-dual-boot)
    * requires a bit more experience since there is more you can destroy
    * better computation performance
2. **Virtual machine:** Linux lives inside your existing operating system.
    * no risk when installation fails
    * less performance because host and guest OS run simultaneously, but usually enough to get started
    * For Windows as a host system, [VMware](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html) ([Installation Tutorial](https://ubuntu.tutorials24x7.com/blog/how-to-install-ubuntu-20-04-lts-on-windows-using-vmware-workstation-player)) is probably the most common software for virtual machines. An alternative is [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
    * For macOS as a host system, you can use the commercial product [Parallels](https://www.parallels.com/).
