## Troubleshooting common installation problems

Here's some common problems that people have and how to get past them.

### SSL errors

A common error people are seeing when they run the command
`conda env create -f ~/Downloads/swc_environment.yaml`
is that it printes error messages with text like 
"CondaSSLError", 
"Exception: HTTPSConnectionPool",
"SSL: CERTIFICATE_VERIFY_FAILED".

If this looks familiar, you can do the following:

- On that same "terminal" as you ran the command that starts with "conda",
  paste in the following command: `conda config --set ssl_verify False`
- Press enter to run that.
- Then, paste in and run (with enter) the command
  `conda env create -f ~/Downloads/swc_environment.yaml`

You'll know that it's working if it says something like
"Collecting package metadata". At this stage, it takes probably 5 minutes to
download and setup the environment.

By the way, if you put the `swc_environment.yaml` file somewhere else other
than in your Downloads folder, you'll need to
specify that. But if it's in your normal `Downloads` folder, you're good to
use `conda env create -f ~/Downloads/swc_environment.yaml` .

### `'$' is not recognized...`

This error message is because the "$" isn't _actually_ part of the command you
want to run.

A fast way to fix this is to:

- Press up-arrow (which will "paste" the last command back up in the terminal).
- Then you can use the arrow keys to go to the "$" and delete the "$" 
  with backspace. 
- Then press enter to run the command.



### How do I open a `bash` terminal / window in MacOSX?

Run the "Terminal" app. 

You should see a mostly white background window show
up with the txt. It might say "zsh" somewhere in the title of the window.
Congrats, you are now using a terminal!

### How do I open a `bash` terminal / window in Windows?

Once you installed the "Git for Windows" installer (in the bash section above),
then

- Press the "Windows" icon key to open up your Start menu.
- Find the "Git Bash" application. 

  Depending on your version of Windows, you
  might want to type "Git" into a searchbar, or browse through menus of 
  Programs until you find the "Git Bash" application under "G".

- Run the "Git Bash" application. You should see a window open up with text,
  and if you type in `ls` and press enter, it should list off some files on
  your system. Congrats, you are now using a terminal!

### Files are failing to open in a "Brackets" application

In the instructions above, we've asked you to download and use some files.
For some of those files, if you have a program called "Brackets" installed
then if you try to open these files by clicking on them, then it may try
to run these files (and fail with an error window!).

Instead, just save them in the usual place (likely the `Downloads` folder),
then try using the terminal commands we provided above.

### If I already have another version of Python installed, will that be a problem?

Very probably not! 

We are using these "conda" tools to install and keep separate all the software
and libraries we are installing for the workshop (python, jupyter, pandas, 
etc). This means that when you successfully "activate" the "swc-gapminder"
environment, it should be using the "swc-gapminder" version of python only.
If you don't activate it, then it shouldn't use this.

So you shouldn't have any problems with other versions of Python.

### Do I have to use `nano` as an editor?

`nano` is a great simple editor for use in the terminal and we recommend it.
If you know how to use a terminal-based text editor like `emacs`, `vim`, 
or `ed`, those options also work. 
If you don't know about these, then we recommend just using `nano`.

