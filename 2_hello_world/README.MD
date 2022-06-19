# Jupyter Notebook

![New notebook](/assets/new_notebook.png)

A **notebook** is a place where you can write pieces of your code in separate **cells** and run them separatly to see the outcome of that piece of code.

Typical IDE's - especially for other languages - dont allow for that. Your code is run in the order it was written in its entirety. 

Python allow for interactive sessions - where a python instance is run in the background and it awaits new commands and process them as they arrive.

This creates a great enviroment (that word again?) for experimantation and allows to quickly test how specific parts of your code works without running entire thing.

Lets try something simple.

# Hello World

Lets get familiar with the interface. Please copy-pase following into the lone cell of our notebook and click **Run** button:
``` 
print("Hello World")
```

![Hello](/assets/helloworld.png)

You will notice few things:
* `In [ ]` changed into `In [1]`
* A new cell appeared below the first one
* New cell is now selected (outline with blue bar on the left side)
* Most importantly `Hello World` appeared under the first cell

Lets break down what just happened.

After we pressed **Run** the code in previously selected cell was executed. This code, as you migth have gessed, simply prints the words "Hello World". All prints and outputs of your code will always show up below the code cell it belongs to.

Since we send command to Python for excecution Jupyter annotated it with numeric number - number 1 - denoting thats it is first command in this session sent to Python interpreter, hence the `In [1]` - Input number 1. Once we have a lot of cell in our notebook it allow us to quickly see which cells where already executed and in which order.

Since that cell was the last cell in our notebook default action of **Run** button is to create new cell at the bottom and select it.

If we now click on the first cell and click **Run** again we will notice that the number changed to `In [2]`, the second cell is selected but no new cell was created.

Now lets type following into second cell and click **Run**:
``` 
1+2
```

![Calculator](/assets/calc.png)

Even though we haven't wrote `print` this time we still see some sort of output of our command. But this time its prefaced with `Out[3]`. What happenes is that python interactive interpreter by default will take last command and send result of it (if possible) to the notebook and it is displayed as `Out` - Output. We alse see that python understand basic arythmetic :) since `3` is correct output for `1+2`.

We can change the ordering of the cells by using **up/down arrows** next to **Run** button. It moves the selected cell up (or down) by one. Notice that cell moves toghether with its output. 

![Reorder cells](/assets/reorder.png)

We can add more cells where we need them using the **+** button. It adds new cell below the selected cell. We can also use **Insert** menu where we can choose if the new cell is insterted above or below

![Add cell](/assets/addcell.png)

We can finally name our notebook as right now it is named "Untitled" and I think we can find better name. To change name simply click on the notebook name at the top of screen and type in new name.

![Rename notebook](/assets/name.png)

**It is good practice to not use spaces in names of notebooks as the notebook name is part of name of file containing that notebook and we dont want spaces in file names. Same goes for directories. It makes automation much easier later where accessing files/paths containing spaces require us to bend over backwards. It will still work but require more work from us to make it so.**

You will notice next to notebook's name there is a timer - how long ago last save was performed. By default Jupyter *should* autosave every now and then, but I learned the hard way not to rely on this behaviour. To save simply click the save icon or select **Save and Checkpoint** in the **File** menu. You can also use `Ctrl+S` keyboard shortcut.

Last thing before moving on: **Markdown** cell. Not every cell have to contain code. It woould not be a very good notepad if we could not scribble some notes here and there.

If we selct a cell we can see what type of cell it is in the same area where all action butons are - there will be a dropdown list with **Code** option selected. We chan change that to **Markdown** to make that cell essentiallly a free text cell (with some formatting options).

![Markdown cell](/assets/markdown1.png)

First thing we notice after switching mode to **Markdown** is dissapearence of `In [ ]`. Since this cell will not be part of our code we no longer need to keep track of its number.

Lets type some random notes in there and run it and see what happens.

![Markdown cell](/assets/markdown2.png)

The edit box dissapeared and was replaced by plain text rendered on screen with no special annotation. You can still select it to see its separate cell from other cells but can type text there. To change it you have to double click on it, this will show the edit box allowing you to change the text.

Markdown allows for many basic formatting options, like headings, bolding, italics, inserting pictures, links to webpages, rendering simple tables, etc - more on that in sections below.



If you want you can read next part if you want to learn how to more efficienntly work with notebook or skip it and go to next chapter.

# Extra: common keyboard shortcuts, command mode and edit mode

Lets start with command modes. Noticed that selected cell have outline and a thin colored bar on the left side. that bar is either blue or green - depending on which mode we are in. 

* If it is green we are in **Edit mode**. In Edit mode we can change the content of the cell, add, delete code, select part of code and copy it or paste code into cell, etc.
* If it is blue we are in **Command mode**. In Command mode we cant interact with the content od the cell but we can interact with entire notebook.

When you are in **Command mode** press `Enter` to enter **Edit mode**. This will change color to green and you can now edit selected cell.

When you are in **Edit mode** press `Esc` to enter **Command mode**. This will change color to blue and you can now access notebook functionality.

Comman mode shortcuts:

|Shortcut|Effect|
|---|---|
|Up/Down Arrow|change selected cell to one above or below|
|`a`|insert new cell above selected cell and selected newly added cell|
|`b`|insert new cell below selected cell and selected newly added cell|
|`dd`|delete selected cell|
|`z`|undo deleting of cell|
|`m`|change cell to Markdown|
|`y`|change cell to code|
|`Ctrl+s`|save notebook|
|`c`|copy entire cell and its output|
|`x`|cut entrire cell and its output|
|`v`|paste copied/cut cell below selected cell|
|`Ctrl+Enter`|Run selected cell, no new cell is created, selection stays at executed cell|
|`Shift+Enter`|Run selected cell, new cell is created below if at the end of notebook, selection moves to cell below|
|`Alt+Enter`|Run selected cell, new cell is created below, selection stays at executed cell|


# Extra: Markdown basics

[There is a great guide](https://www.markdownguide.org/basic-syntax/) on Markdown and I strongly advise to bookmark that page and reference it later, but for now here are few most common formatting options and how to achieve them:

**Bold**
`**text**`
**text**

**Italic**
`*text*`
*text*

**Headings**
```
# Heading 1

## Heading 2

### Heading 3
```

# Heading 1

## Heading 2

### Heading 3

**URL**
`[Friendly name](www.google.com)`

[Friendly name](www.google.com)

**Image**
`![Alternate display - in case file not available](/assets/calc.png)`

![Alternate display - in case file not available](/assets/calc.png)

`![Alternate display - in case file not available](/assets/no_such_file.png)`

![Alternate display - in case file not available](/assets/no_such_file.png)

**Ordered list:**
```
1. text 1
1. text 2
1. text 3
    1. sub text 1 indented by 4 spaces or tab
    1. sub text 2 indented by 4 spaces or tab
1. text 4
```

1. text 1
1. text 2
1. text 3
    1. sub text 1 indented by 4 spaces or tab
    1. sub text 2 indented by 4 spaces or tab
1. text 4

**Unordered list:**

```
* text 1
* text 2
* text 3
    * sub text 1 indented by 4 spaces or tab
* text 4
```

* text 1
* text 2
* text 3
    * sub text 1 indented by 4 spaces or tab
* text 4

**Blockquotes**
`> Now these points of data make a beautiful line.`

> Now these points of data make a beautiful line.

**Code**
```Only `this part` will be rendered as code```

Only `this part` will be rendered as code

**Code block**

```
    use 4 space
    before each line
    or a tab
    so this entire
    thing will
    be rendered 
    as code
```

    use 4 space
    before each line
    or a tab
    so this entire
    thing will
    be rendered 
    as code

````
```
Or use tripple backtics
so this entire
thing will be rendered 
as code
```
````

```
Or use tripple backtics
so this entire
thing will be rendered 
as code
```