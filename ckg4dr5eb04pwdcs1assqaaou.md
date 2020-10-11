## Creating and Automating Backups with BASH Scripts

Backup is a very common routine in today's world now. Anyone can easily backup documents on external hard drives or in the cloud storage system like Google Drive, DropBox, OneDrive, etc. Generally, people use any of these free cloud storage or external hard drives for backing up documents. But you can easily create an automated script that does that for you every day.

By the end of this article, you should be able to:

- Create a simple bash script that backups your `Documents` folder
- Learn how to automate/ schedule the backup task


## Initialization

You can use any text editor or a command-line editor like nano to create your script. I will be using the Visual Studio Code for the purpose of this tutorial. 

Open the terminal `Ctrl + Alt + D`, and create a file `backup_script.sh`. Rememmber to use the `.sh` extension.

```bash
touch backup_script.sh
```

**Open in vscode**

```bash
code backup_script.sh
```

The code of your `backup_script.sh` will be the following:

```bash
#!/bin/bash

#Backup Location
BACKUP_PATH="$HOME/Documents"

#Create a directory "backup"
mkdir $HOME/backup

#Where to backup to
DEST_PATH="$HOME/backup/"

#Create date for backup and archive filename
DATE=`date +%d%m%Y`
BACKUP="doc_"
EXT=".tar"
FILE_NAME=$DEST_PATH$BACKUP$DATE$EXT

#Print a status message to the console
echo "Hey $USER, Backing up $BACKUP_PATH to $FILE_NAME"
date
echo

#Copy files from Document to the Backup directory.
tar cfz $FILE_NAME $BACKUP_PATH

#Print end status message
echo
echo "Backup finished"
date

# Long listing of files in the destination path to check file sizes.
ls -lh $FILE_NAME 

```

## The important commands here

`#!/bin/bash`

Known as **"she-bang(shabang)"**, also called as **sh-bang, hashbang, poundbang, or hash-pling**. Is the character sequence consisting of the characters number sign and exclamation mark (#!) at the beginning of a script.

`tar cfz $FILE_NAME $BACKUP_PATH`

Known as **tarball**, is a utility for collecting many files into one archive file. Works as **zip** you could be familiar with that.

`cfz`

- c: create
- f: use archive file or device ARCHIVE 
- z: compress the files to reduce the size

Most of the other commands were declaring variables and printing them to the console.

## Running your task

To run the backup script, from your terminal or the embedded vscode terminal, run the following command to make our script executable:

```bash
chmod +x backup_script.sh
```

**To run our script:**

```bash
./backup_script.sh
```
> 
Relax and take some coffee while the tasks are backing up your documents

Once the backup is completed, you will see the message `Backup finished` on your terminal open the Home directory and you should see a `backup` directory with your backup. 

*Congratulation on making it this far, you should be proud of yourself.*

<img src="https://media1.tenor.com/images/2386d12e54aa11ce0298d100954d982a/tenor.gif?itemid=4384522" alt="Congratulation Image"/img>

## Schedule your Backup Task

We're going to use `cron`, also called `cron job` a Linux / Unix time-based job scheduler. This utility allows you to schedule tasks to run at a specific time in the future.

Save your bash script and close the editor and open the terminal again. To edit the crontab file with the editor you prefer (**nano is the easiest**), run the command:

```bash
crontab -e
```
Let’s understand the contrab line format:

minute(0–59) hour(0–23) day(1–31) month(1–12) weekday(0–6)

Let’s say that we want to run the script every day at 12:30 a.m. we would type this at the end of the crontab file:

```txt
29 0 * * * /bin/bash /$HOME/backup_script.sh
```

- **29**: stands for the 30 minute 
- **0**: stands for 12AM
- The first `*` stands for every day
- The second `*` stands for every month
- The third `*` stands for every weekday
- /path/to/command – Script or command name to schedule

Use `Ctrl + S` to save your crontap file, and `Ctrl + X` to exist the `nano` editor. That's it, congratulation again, you have done a great job.

To remove or erase all crontab jobs use the following command:

```bash
crontab -r
```

Visit https://crontab-generator.org to generate a crontab line of your choice.

<hr>

I hope this article was helpful. If so, share this article and follow [me on Twitter](https://twitter.com/IrolehVincent) 