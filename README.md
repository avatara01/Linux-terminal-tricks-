
# Cool Linux terminal tricks to save time and increase productivity

You might already know a few of these Linux command tips or perhaps all of it. In either case, you are welcome to share your favorite tricks in the comment section.

Some of these tips also depend on how the shell is configured. Let’s begin!

## 0. Using tab for autocompletion

I’ll start with something really obvious and yet really important: tab completion.

When you are starting to type something in Linux terminal, you can hit the tab key and it will suggest all the possible options that start with string you have typed so far.

For example, if you are trying to copy a file named my_best_file_1.txt, you can just type ‘cp m’ and hit tab to see the possible options.

## 1. Switch back to the last working directory

Suppose you end up in a long directory path and then you move to another directory in a totally different path. And then you realize that you have to go back to the previous directory you were in. In this case, all you need to do is to type this command:
```
cd -
```

This will put you back in the last working directory. You don’t need to type the long directory path or copy paste it anymore.

## 2. Go back to home directory

This is way too obvious. You can use the command below to move to your home directory from anywhere in Linux command-line:
```
cd ~
```
However, you can also use just cd to go back to home directory:
```
cd
```
Most modern Linux distributions have the shell pre-configured for this command. Saves you at least two keystrokes here.

## 3. List the contents of a directory

You must be guessing what’s the trick in the command for listing the contents of a directory. Everyone knows to use the ls -l for this purpose.

And that’s the thing. Most people use ls -l to list the contents of the directory, whereas the same can be done with the following command:
```
ll
```
Again, this depends on the Linux distributions and shell configuration, but chances are that you’ll be able to use it in most Linux distributions.

## 4. Running multiple commands in one single command

Suppose, you have to run multiple Linux commands one after another. Do you wait for the first command to finish running and then execute the next one?

You can use the ‘;’ separator for this purpose. This way, you can run a number of commands in one line. No need to wait for the previous commands to finish their business.
```
command_1; command_2; command_3
```

## 5. Running multiple commands in one single command only if the previous command was successful

In the previous command, you saw how to run several commands in one single command to save time. But what if you have to make sure that commands don’t fail?

Imagine a situation where you want to build a code and then if the build was successful, run the make?

You can use && separator for this case. && makes sure that the next command will only run when the previous command was successful.
```
command_1 && command_2
```
A good example of this command is when you use sudo apt update && sudo apt upgrade to upgrade your system.

## 6. Easily search and use the commands that you had used in the past

Imagine a situation where you used a long command couple of minutes/hours ago and you have to use it again. Problem is that you cannot remember the exact command anymore.

Reverse search is your savior here. You can search for the command in the history using a search term.

Just use the keys ctrl+r to initiate reverse search and type some part of the command. It will look up into the history and will show you the commands that matches the search term.
```
ctrl+r search_term
```
By default, it will show just one result. To see more results matching your search term, you will have to use ctrl+r again and again. To quit reverse search, just use Ctrl+C.
Note that in some Bash shells, you can also use Page Up and Down key with your search term and it will autocomplete the command.

## 7. Unfreeze your Linux terminal from accidental Ctrl+S

You probably are habitual of using Ctrl+S for saving. But if you use that in Linux terminal, you’ll have a frozen terminal.

Don’t worry, you don’t have to close the terminal, not anymore. Just use Ctrl+Q and you can use the terminal again.
```
ctrl+Q
```

## 8. Move to beginning or end of line

Suppose you are typing a long command and midway you realize that you had to change something at the beginning. You would use several left arrow keystrokes to move to the start of the line. And similarly for going to the end of the line.

You can use Home and End keys here of course but alternatively, you can use Ctrl+A to go to the beginning of the line and Ctrl+E to go to the end.

I find it more convenient than using the home and end keys, especially on my laptop.


## 9. Delete entire line from cursor position

So many people either do not know about it or hardly use it.

In the Linux terminal, if you press Ctrl+U, it deletes everything from your current cursor position to the beginning of the line.

Similarly, if you press Ctrl+K, it deletes everything from your cursor position to the end of the line.

Possible made a mistake in typing the password? Instead of using backspace key all the way, simply use Ctrl+U and retype the password. You can discover plenty of other uses for these shortcuts.

## 10. Reading a log file in real time

In situations where you need to analyze the logs while the application is running, you can use the tail command with -f option.
```
tail -f path_to_Log
```
You can also use the regular grep options to display only those lines that are meaningful to you:
```
tail -f path_to_log | grep search_term
```
You can also use the option F here. This will keep the tail running even if the log file is deleted. So if the log file is created again, tail will continue logging.


