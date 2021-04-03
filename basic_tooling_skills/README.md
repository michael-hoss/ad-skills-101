# 🔧 Tooling skills for programming

Even if you can write perfect source code, you still need to master a lot of tooling to get your project running. 


## 💻 Setting up a Linux operating system

Linux is orders of magnitude more popular for R&D in automated driving than Windows or Mac. Check out [how to set up a linux operating system](Setting_up_Linux.md) and continue working in Linux.


## 🛠️ The Missing Semester of your computer science education

Now that you have a working linux distribution, you can learn using it well. 
Even in computer science curricula themselves, some essential applied skills are never officially taught. Therefore, the MIT has introduced [**The Missing Semester of Your CS Education**](https://missing.csail.mit.edu/), a lecture series on YouTube that covers very basic computer science tooling, namely command line interface and shell scripting, text editors, version control, debugging, virtual machines, remote machines, finding files, data wrangling, and more. 

It is extremely helpful to learn those skills before continuing with the content below.



## 🐢 ROS

[ROS](https://www.ros.org/) (Robot Operating System) is THE most essential software framework for prototyping automated driving functions. It facilitates and standardizes many activities of function developers, such as
- defining individual processes of computation (ROS nodes) 
- defining interfaces for communication between these processes (ROS messages exchanged through ROS topics)
- recording and replaying these messages (`rosbag record` and `rosbag play`)
- visualization (RViz)
- organizing your source code in packages for easier exchange and re-use (catkin/colcon packages)

If you are a student of RWTH Aachen University, you can learn ROS in the context of automated driving with the [Self-Driving Lab I - Software Framework](https://git.rwth-aachen.de/ika/sdl1-ws2020) materials from RWTH's GitLab. 

In any case, the [official ROS tutorial](http://wiki.ros.org/ROS/Tutorials) is an excellent source for learning ROS in general.  




## :octocat: Version control with Git

One of the tools that can leverage the productivity of you and your team most is a proper version control system for your source code. So far, you might have experienced a workflow where each contributor works in their own folder and then renames it "source_code_v37" before uploading it on a shared folder in a cloud. The next contributor would copy-paste this folder, do local changes, rename it "source_code_v38" and upload it again next to the folders of the previous versions. 

In this setting, chances are that you do not enjoy working simultaneously, resolving conflicts, going back farther than <kbd>Ctrl</kbd>+<kbd>Z</kbd> allows, or tracing back whom to ask regarding a specific code part. 

The good news is that the version control system Git makes all of these things super easy, so you should definitively learn it! Terms to differentiate are:
- Git: the version control system itself; it is a local command line application
- GitHub: the most popular website/online service for hosting open source Git repositories, such as this one.
- GitLab: similar to GitHub, but you can also install a free version of it on your own server.
- GitFlow: a workflow for the integration of multiple software features from different developers into a single stable version
- GitKraken: a GUI (graphical user interface) for Git that helps you manage your Git repository.


## IDEs

### IDEs for C++

CLion, QtCreator (with ROS plugin)

### IDEs for Python 

PyCharm


## Language-specific tooling 


### Tooling for C++ 

CMake, make, compiling, linking, static and shared libraries, how to include files etc.


### Tooling for Python 

conda and pip, virtual environments, PiPy, difference between a package and a module, what does an `__init__.py` file do? etc.

