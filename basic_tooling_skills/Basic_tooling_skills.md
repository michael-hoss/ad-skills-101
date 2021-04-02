# 🔧 Tooling skills for programming

Even if you can write perfect source code, you still need to master a lot of tooling to get your project running. 


## *computer emoji* Setting up a Linux operating system

Linux is orders of magnitude more popular for R&D in automated driving than Windows or Mac. Check out [how to set up a linux operating system](Setting_up_Linux.md) and continue working in linux.


## *tool emoji* The Missing Semester of your computer science education

Take this from the blog article.

Now that you have a working linux distribution, ...

A round trip of all kinds of important fundamentals: 

possible to embed links somehow?
https://missing.csail.mit.edu/

## *robot emoji* ROS

ROS (Robot Operating System) is THE most essential software framework for prototyping automated driving functions. It facilitates and standardizes many activities of function developers, such as
- defining individual processes of computation (ROS nodes) 
- defining interfaces for communication between these processes (ROS messages exchanged through ROS topics)
- recording and replaying these messages (`rosbag record` and `rosbag play`)
- visualization (RViz)
- organizing your source code in packages for easier exchange and re-use (catkin/colcon packages)

If you are a student of RWTH Aachen University, you can learn ROS in the context of automated driving with the [Self-Driving Lab I - Software Framework](https://git.rwth-aachen.de/ika/sdl1-ws2020) materials from RWTH's GitLab. 

In any case, the [official ROS tutorial](http://wiki.ros.org/ROS/Tutorials) is an excellent source for learning ROS in general.  




## *kraken emoji* Especially important: version control with Git

Take some text from the blog post.

One of the tools that can leverage the productivity of you and your team most is a proper version control system for your source code. You might have  experienced a workflow before where each contributor works in their own folder and then renames it "source_code_v37" before uploading 

Git, GitHub, GitLab, GitFlow

GitKraken



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

