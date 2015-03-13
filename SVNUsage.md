# SVN Usage #
This page covers the sections of the SVN and their usage
http://code.google.com/p/teamkomin/source/browse/


## Breakdown of Folders and Functions ##
This section covers Folders and Functions out of the Team Komin SVN repository

The SVN is broken down into sections:
  * Trunk
  * Distributions
  * Branches
  * Wiki
### Trunk ###
The trunk is where active development takes place.  This folder is used to create distributions after it is agreed that the repository is in a state which is ready for release. Most developers will select this for their SVN checkout repositories.
### Distributions ###
The distributions section is broken down into Current and Archives. The Archives contains previous versions of Andromeda.   Current contains the latest version of Andromeda at all times.
### Branches ###
Generally branches are testing repositories where any member can spawn a new version of the Trunk for testing purposes.
### Wiki ###
You are reading the wiki right now. The wiki is kept under SVN version control for revision and reversion.

## Development ##
This section covers checkout, update, work, and check-in

The Development cycle consists of:
  * Checkout or Update
  * Work
  * Check-in


#### SVN Checkout(CO) ####
During a SVN CO operation, all information in the selected repository is synchronized one-way to your computer.  For all purposes except branching, the SVN repository used is Trunk

  * Repository -https://teamkomin.googlecode.com/svn/trunk/
  * Username   -Your username is your Google developer email address
  * Password   -Obtain your password here:http://code.google.com/hosting/settings

Checkout needs to be performed only once.  After the first CO, you will use Update.

#### SVN Update(up) ####
At the beginning of a work cycle, you should always SVN up to ensure you are working with the latest code.   SVN up will synchronize changes from the server to your computer.

#### work cycle ####
All files must be added or removed from SVN revision control.   SVN add and SVN delete commands are commonly used.  Sometimes a SVN revert command is issued when a file reversion is required.

#### SVN Commit(ci) ####
SVN Commits are used at the end of a work cycle to commit changes.  They can also be used to add notes when committing single files.


## Testing ##

Under linux,
  * copy all folders in Trunk to a new directory on your desktop.
  * From the terminal, cd to the folder and type:
> `find . -name ".svn" -type d -exec rm -rf {} \;`
  * Then from the desktop right click all folders in trunk and compress to zip.
You are now ready to test


Remember, you can always delete your repository and svn co https://teamkomin.googlecode.com/svn/trunk/ later in case of emergency.