# :brain: Software project skills

Naturally, your projects grow to a size where the source code and the architecture become messy, more and more bugs occur, and fixing one creates another. Therefore, you should learn to avoid those struggles and instead do what is necessary to let your project sustainably grow over time.

### Clean code

If you know the pain of having to use someone else's dirty code or even your own code from some time ago, then you might be motivated to learn how to write clean code. Some essential rules are:
- Use *descriptive names* for variables, functions, classes, files etc. Ideally, all your naming tells such a self-explaining story that you hardly need any comments anymore.
- Use *short functions and classes*: they should each be responsible for only one thing, and do that thing well. Having such small building blocks facilitates re-assembling and re-using them.
- Have a *consistent level of abstraction* to keep the overview: e.g., calling your most important high-level function should not happen in between some detailed string manipulations.

Further resources:

| Resource | Description | Recommendation |
| --- | --- | ---- |
| [Clean Code](https://www.oreilly.com/library/view/clean-code-a/9780136083238/) | A classical book for software developers | Read this to make your future code cleaner. Examples are given in Java, but the concepts are really helpful for all languages.  |
| [Refactoring Guide](https://sourcemaking.com/refactoring/refactorings)  | Website that explains all sorts of ways how you can improve already written code | Learn this if you have an existing project whose code you find harder and harder to understand |



### Clean architecture

A project with a clean architecture is like Lego blocks that you can easily rearrange. Lego blocks have clearly defined shapes, interfaces, and you know how to stack them on top of each other to build something stable. <!-- You can take the roof of one Lego house and put it on a completely different Lego house as long as the blocks structure supporting the roof is the same. -->
A project with a bad architecture is like a ball of filthy wool.  Trying to use one specific part of wool from the middle means deforming and destroying the entire ball. Even then, you can hardly be sure whether you got that piece of wool that you actually wanted.


Those further resources might help you structure your project more like Lego than like wool:

| Resource | Description | Recommendation |
| --- | --- | ---- |
| [Clean Architecture](https://www.oreilly.com/library/view/clean-architecture-a/9780134494272/) | A classical book for software developers | Read this to make your future software architecture cleaner.  |
| [SOLID principles](https://dzone.com/articles/solid-principles-basic-building-blocks-of-a-clean) | Website explaining the so-called SOILD principles of good software architecture | Boiled-down essence of the "Clean Architecture" textbook.  |



### Documenting your project

#### READMEs in markdown syntax

As you might have noticed in this repository, I am a big fan of markdown files (`.md`) because they are easy to write, their contents can be tracked in Git, and they render beautifully in both GitHub and GitLab. Those tutorials help you write good markdown READMEs:
* [GitHub: mastering markdown](https://guides.github.com/features/mastering-markdown/)
* [Interactive lessons on how to learn markdown](https://www.markdowntutorial.com/lesson/1/)

#### Generated documentation from code comments
While self-written markdown is good for higher-level information about your project, you might want to use a dedicated tool to automatically generate the documentation of the lower-level details of your code (files, classes, functions, etc.)

The following tools expect you to structure your code comments according to a certain syntax such that the tool can automatically generate an html or PDF documentation. In modern IDEs, there are plugins available that help you write your comments in that way.

But always remember: a good documentation can be pretty short if you have already used self-explaining names for variables, functions, classes, and files.


| Tool | Supported languages | Description |
| ---  | --------------      | ------ |
| [doxygen](https://www.doxygen.nl/manual/starting.html) | C/C++ (Java, PHP, Python)   | Standard way |
| [pydoc](https://docs.python.org/3/library/pydoc.html) | Python | Standard way |
| [Sphinx](https://www.sphinx-doc.org/en/master/usage/quickstart.html) | Python | Looks like readthedocs |





### Test-driven development

A lot of software being written in research projects is only tested manually, meaning the developer executes the code and observes whether the code produces the expected result.

The larger your project grows, the less feasible this approach becomes because every time that you don't know why your code misbehaves, you typically don't have the patience to test the 10 different places where something could theoretically have gone wrong.

Therefore, you ideally write tests that automatically check all of these 10 places, and you can execute all of them with the click of a button.

Moreover, you write the tests *before* you write the actual code. This can help you become more aware about what you actually want your code to do. Also, you will know when when your code is "done" - when all the test results have switched from red to green.

Since I don't yet practice what I preach, I welcome recommendations for good material about how to get started with test-driven development.


### Containerization

You might know the phrase "... but it works on my laptop!" when you cannot get someone else's code to work on your own machine.
To avoid struggles like this, people have started executing code not natively on their operating systems, but from within so-called containers.
These containers have the necessary packages installed in their exactly needed versions, have the right environment variables set etc. They can be exchanged such that everyone running a code has the exact same environment.

The most important container technology is Docker. You can imagine it as something more than a virtual environment in Python, but less than a virtual machine.

Recommendations for useful resources are welcome!



### Collaboration tools and techniques

#### Issues and pull/merge requests on GitHub or GitLab
Your code project is usually hosted on GitHub or a GitLab instance anyway, so you can also use the collaboration functionalities that these platforms bring.

Check out for example:
[YouTube Video: Lecture 2.0 - Github : Issues and Pull Requests](https://www.youtube.com/watch?v=LuL60r-XnL4)

#### Chats

Perhaps the most common chat programs for companies and especially software developers are Slack (closed-source) and Mattermost (open-source version exists).



#### Kanban board

Without going too much into the details of agile software development, the concept of a Kanban board can help you organize the work in your internship or thesis.

Check out for example:
[Kanban Tutorial: How to Setup a Kanban Board](https://www.youtube.com/watch?v=7MDWfAsrrtw)

Many software tools offer digital Kanban boards, for example in GitLab you can display your issues as a Kanban board.






### Continuous integration (CI)
You might have experienced the situation where a colleague has merged bad code into the main Git branch, and suddenly it doesn't work anymore.
They should have tested their code with the entire test suite before pushing it!
Fortunately, both GitHub and GitLab provide you with many possibilities to test commits online. You can allow merges only if all tests pass, which keeps your main branch stable and usable at all times.

In other words, you continuously integrate your changes into the always-stable main version. Like this, you are able to merge your work multiple times per day! Otherwise, a giant merge of everything you did at the end of your thesis/internship into your colleagues' main project might become too difficult to actually succeed.

Useful material in this context:

| Resource | Description | Recommendation |
| --- | --- | --- |
| GitHub Actions | Mechanism to execute tests in GitHub | |
| GitLab Runners | Mechanism to execute tests in GitLab | |
| TravisCI | Exemplary third-party tool to integrate in GitHub for executing tests  |
| The DevOps Handbook | Well-written book that describes the need for such techniques and how to implement them on a high level | |
