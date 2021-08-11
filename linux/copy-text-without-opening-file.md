# How to copy sensitive text data without opening the text file in editor?

## Why needed?
Why do you need to copy text without opening in an editor? 

Let me explain briefly.

You might be working with sensitive data, e.g. some configuration file, or some ssh key file that you need to copy & paste in a password field for completing some configurations.

Since you will be pasting the copied content to password or secret field it will not be visible, but the problem is when you copy the content by openining the file the content is visible in your editor.

So, let's see, how you can copy the sensitive content without opening the text file in text editor-

## Steps Required

### Step#1
For copying without opening file in text editor we will be using ```xclip```

So, to install ```xclip``` follow the bellow instructions-

```bash
$ sudo apt-get update
$ sudo apt-get install xclip
```

### Step#2
Now to copy the content of text file without opening it, run the following command-

```bash
$ xclip -selection clipboard < your_text_file.txt
```


This command will copy the content from ```your_text_file.txt``` file.

### Step#3
Now you can paste the copied content anywhere. So, that's it, you have just copied the content of a text file without visibly opening the sensitive data in an editor.


**N.B. This approach is tested in Ubuntu 16.04, 20.04 & Gnome environment. Might not work in other systems. Please check your system environment before running this task.**

