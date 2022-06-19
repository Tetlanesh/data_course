# Installing Python

We will start our course with installing python on Your computer. We will focus on Windows enviroment for this part of the course, but I will include link to instruction for other systems.

If we look 10 years back installing Python on windows with goal of working with data was difficult if You wanted to do anything more than most basic stuff. Different libraries that we rely on when working with data have different required dependencies (other software/library needed by it to work) and it was not unusual to find out that library that we need simply dont work on windows or it have conflict with diffrent library. Since then we got [Anaconda](https://www.anaconda.com/products/distribution) - a Python distribution that solved most of the issues.

First we need to download [Anaconda](https://www.anaconda.com/products/distribution). There is download option for Windows, MacOS and Linux. Click on your operating system icon and select the correct installer for your system architecture (probably 64-bit unless your pc is 10 years old).

During instalation You will be asked to set anaconda as your default Python interpreter - its important to leave all options as they are and not to change anything from default state.

![anaconda isntallation](/assets/anaconda.png)

Once installed you should be able to find two application after typing anaconda into your start menu:
* Anaconda Navigator - a graphical interface that allows you to customise your development environment but only to the limits allowed by the interface
* Anaconda Prompt - a text terminal that allows us to do the same and more

![start menu](/assets/startmenu.png)

But for a quick start and getting our feet wet we will start with Navigator for now. Run **Anaconda Navigator** from your start menu. After a brief loading You should see screen similar to this:

![Anaconda navigator](/assets/navigator.png)

First thing is to create a new enviroment. 

# Enviroments

What is enviroment and why do I need it?

Quoting from [conda documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/environments.html):

> A conda environment is a directory that contains a specific collection of conda packages that you have installed

But what does it mean?

As you will inevitably learn there are many version of Python and many versions of libraries for Python. And they are not necessarily compatible with each other. Imagine you wrote an application (lets call it App1) that is now beeing used by your company. It requires specific versions of libraries to run and you installed all of them on your pc when you worked on that program. Now you want to work on new application (App2) and you want to use that new fancy library everyone on the internet is talking about, but when you try to install it you got message that it need to upgrade some of those already installed libraries and maybe even downgrade others. Image if you will that you suddenly want to make update or fix for App1... and it does not even run anymore or worse - it runs but produce incorect results. It relied on specific versions of python and versions of libraries to run and those changed when we installed.

If only we could somehow separate those two project into their own... what to call them... **enviroments**?

Thats exactly what enviroments are for. They separate different sets of installed libraries and python versions into their own separate boxes that you can switch between when needed. You can safely install new libraries to one enviroment and not have to worry that it will break another.

Its critical that you will keep your enviroments separate for every projects you will create and thats why we are starting with that specific task before we even wrote our "hello world". Luckily Conda Navigator have a very easy to use enviroment creator so lets start. 

# Lets create our first enviroment

Go to **Enviroment** tab (on left side of screen) than select **Create** button on the bottom. You will be asked to give name to your enviroment and select python version.

![New Enviroment](/assets/newenv.png)

Lets pick python version at least 3.9 (my version allows for 3.10 but if you are reading this in the future yours may have different version avaialble) and click **Create**. After (hopefully) brief time the enviroment is created and we can activate it by clicking on its name in enviroment list. It will turn green when you do.

![Activate](/assets/activate.png)

Now that we created our enviroment we need a tool for writing code. An IDE - Interactive Development Enviroment. An application that facilitates writing and executing your code and displays results. Luckily Anaconda comes with few options. During the course we will use at least 2 IDE's for Python but for now lets meet our first IDE: **Jupyter Notebook**.

Go to **Home** tab and find **Jupyter Notebook** on application board. It should have green **Install** button availalble. Click it and wait untill it finish than click blue **Launch** button.

![Install Jupyter](/assets/jupyter_install.png)

When you do you will notice that your browser start on a new tab with a view similar to this:

![Jupyter](/assets/jupyter.png)

It should by default show the content of your user folder. We cant change that right now - dont worry, we will have full control over where we want to keep our code soon enough, but for now lets play along.

In right top corenr there is a **New** button that allows us to create - among other things - new python notebooks and new folders. Lets keep our user folder clean and create new folder. It will show up on the list as "Untitled folder". Select it (checkbox next to it) and select **Rename** at the top to give it a new name. 

![Rename](/assets/rename.png)

Once you are ready enter that folder (by clicking on its name) and create a new Python notebook. When you do your browser will open a new tab with your bran new notebook:

![New notebook](/assets/new_notebook.png)

