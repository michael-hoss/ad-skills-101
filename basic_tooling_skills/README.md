# 🔧 Tooling skills for programming

Even if you can write perfect source code, you still need to master a lot of tooling to get your project running.


## 💻 Setting up a Linux operating system

Linux is orders of magnitude more popular for R&D in automated driving than Windows or macOS. Check out [how to set up a linux operating system](Setting_up_Linux.md) and continue working in Linux.


## 🛠️ The Missing Semester of your computer science education

Now that you have a working linux distribution, you can learn using it well.
Even in computer science curricula themselves, some essential applied skills are never officially taught. Therefore, the MIT has introduced [**The Missing Semester of Your CS Education**](https://missing.csail.mit.edu/), a lecture series that covers very basic computer science tooling, which is also [available on YouTube](https://www.youtube.com/channel/UCuXy5tCgEninup9cGplbiFw). Here are the copy-pasted contents:
- Course overview + the shell
- Shell Tools and Scripting
- Editors (Vim)
- Data Wrangling
- Command-line Environment
- Version Control (Git)
- Debugging and Profiling
- Metaprogramming
- Security and Cryptography
- Potpourri
- Q&A

It is extremely helpful to learn those skills before continuing with the content below.


## 🐢 ROS

[ROS](https://www.ros.org/) (Robot Operating System) is THE most essential software framework for prototyping automated driving functions. It facilitates and standardizes many activities of function developers, such as
- defining individual processes of computation (ROS nodes)
- defining interfaces for communication between these processes (ROS messages exchanged through ROS topics)
- recording and replaying these messages (`rosbag record` and `rosbag play`)
- visualization (RViz)
- organizing your source code in packages for easier exchange and re-use (catkin/colcon packages)

If you are a student of RWTH Aachen University, you can learn ROS in the context of automated driving with the [Self-Driving Lab I - Software Framework](https://git.rwth-aachen.de/ika/sdl1-ws2020) materials from RWTH's GitLab.

In any case, the [official ROS 1 tutorial](http://wiki.ros.org/ROS/Tutorials) is an excellent source for learning ROS in general.

As of 2021, ROS 1 is still widely used and therefore much ROS software you find in the internet is written in ROS1. ROS 2 is an important update as it provides real-time capability and many more new features. ROS 2 is getting more popular so you may also have a look at the [official ROS 2 tutorial](http://index.ros.org/doc/ros2/Tutorials).



## :octocat: Version control with Git

Git is already covered in *The Missing Semester*, but I cannot stress enough how important it is and therefore dedicate a separate section to it.

One of the tools that can leverage the productivity of you and your team most is a proper version control system for your source code. So far, you might have experienced a workflow where each contributor works in their own folder and then renames it "source_code_v37" before uploading it on a shared folder in a cloud. The next contributor would copy-paste this folder, do local changes, rename it "source_code_v38" and upload it again next to the folders of the previous versions.

In this setting, chances are that you do not enjoy working simultaneously, resolving conflicts, going back farther than <kbd>Ctrl</kbd>+<kbd>Z</kbd> allows, or tracing back whom to ask regarding a specific code part.

The good news is that the version control system Git makes all of these things super easy, so you should definitively learn it!
The following YouTube tutorial seems to cover all essentials.

**[Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk)**.

Furthermore, terms to differentiate are:
- [Git](https://git-scm.com/): the version control system itself; it is a local command line application.
- [GitHub](https://github.com/): the most popular website/online service for hosting open source Git repositories, such as this one. Additionally, the company GitHub releases more and more Git-related software for Desktop computers.
- [GitLab](https://about.gitlab.com/): similar hosting service like GitHub, but you can also install a free and open source version of it on your own server. For example, RWTH has the
  - [premium GitLab version]((https://git.rwth-aachen.de/)) for education, and the
  - [free and open source GitLab version](https://git-ce.rwth-aachen.de) for projects with industry partners.
- [GitKraken](https://www.gitkraken.com/): one of the most popular desktop GUIs (graphical user interfaces) for Git that helps you manage your Git repository.
  - I recommend initially applying all Git commands in the command line. Only like this you will actually understand them!
  - Through GitKraken, you can get a better overview over your Git branches. Once you are confident about a certain Git command, you can also execute it in the GitKraken GUI.
- A *Git workflow*: a way to integrate multiple software features that have been developed by different people on different so-called *Git branches* into one single stable branch. Example video: [A Better Git Workflow with Rebase](https://www.youtube.com/watch?v=f1wnYdLEpgI&t=41s).

## IDEs

An integrated development environment (IDE) is a program that can make it easy for you to program and develop software.
It usually has at least a source code editor, a compiler or interpreter, and a debugger (see also the [Wikipedia article](https://en.wikipedia.org/wiki/Integrated_development_environment)).

For beginners, IDEs are often a "double-edged sword": since IDEs are usually designed for professionals, they have so many features and options for configuration that you can easily get confused and lost.
Therefore, it is usually a good idea to really dedicate some time to understand your IDE and configure it according to your needs.

If you come from an "all-in-one solution" such as MATLAB, the following disambiguation might help you understand what an IDE actually consists of.

| Term | Description |
| --- | --- |
| [IDE](https://en.wikipedia.org/wiki/Integrated_development_environment) | Program that integrates all the other tools into one GUI. |
| [Language](https://en.wikipedia.org/wiki/Programming_language) | Note that a programming language itself can be specified with pen and paper only! See e.g. [C++ standard](https://isocpp.org/std/the-standard). |
| [Compiler](https://en.wikipedia.org/wiki/Compiler) | Program that translates source code to binary code according to the specification of a programming language. This is where the language comes to life. Used for C++. |
| [Interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) | Program that directly executes your code without having to compile it. Used for Python and MATLAB. |
| [Debugger](https://en.wikipedia.org/wiki/Debugger) | Program to test and debug other programs. |
| [Further IDE-provided functionalities](https://en.wikipedia.org/wiki/Integrated_development_environment)  | For example, syntax highlighting, code completion, refactoring, a Git GUI, code search and replace functionalities, a terminal, an object browser etc. |

### IDEs for C++

Many IDEs focus on supporting one programming language only.
The following IDEs are most common for beginners who program ROS nodes in C++.

#### QtCreator

- Maybe the most beginner-friendly way to develop ROS nodes in C++.
- There is a helpful [plugin for ROS1 and its catkin build system](https://ros-qtc-plugin.readthedocs.io/en/latest/index.html).
  - After installation, import your existing catkin workspace [like this](https://ros-qtc-plugin.readthedocs.io/en/latest/_source/Import-ROS-Workspace.html).
  - After importing the `catkin_workspace`, you can use the "Hammer" symbol in the bottom left corner instead of `catkin build`.
- QtCreator's GUI is probably easier to understand than the GUI of more professional IDEs, but it might also have some bugs here and there.


#### [CLion](https://www.jetbrains.com/clion/)
- More advanced and reliable C++ IDE by JetBrains.
- Educational license is available [here](https://www.jetbrains.com/community/education/#students).
- [ROS setup tutorial by JetBrains](https://www.jetbrains.com/help/clion/ros-setup-tutorial.html)
- YouTube video: [Using CLion to edit and build ROS Package](https://www.youtube.com/watch?v=8uH-ghZVDH8).

### IDEs for Python

#### [PyCharm](https://www.jetbrains.com/pycharm/)
- Probably the most common Python IDE.
- The community edition is totally fine for beginners.
- Also by JetBrains, so it is similar to CLion.
- YouTube video: [PyCharm + Ros Setup Guide](https://www.youtube.com/watch?v=lTew9mbXrAs)

### IDEs for both C++ and Python

There are also IDEs that support various languages if they are configured accordingly. The most common are:

| IDE  | Explanation |
|--- | --- |
| [Visual Studio Code](https://code.visualstudio.com/)  | Highly used, good, reliable, and free product from Microsoft, for both C++ and Python. <br> Check out this [YouTube video: How to Setup VSCode for ROS](https://www.youtube.com/watch?v=RXyFSnjMd7M). |
| [Eclipse](http://wiki.ros.org/IDEs#Eclipse) | Highly customizable, but maybe too complex for beginners of C++ or Python?  |
| [ROS IDEs](http://wiki.ros.org/IDEs)  |  Official overview of ROS IDEs, where the IDEs mentioned here are also listed.|


## Language-specific tooling


### [Tooling for C++](Tooling_C++.md)

### [Tooling for Python](Tooling_Python.md)
