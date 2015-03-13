# Autobuilding #
Once you have read and set up your [SVN repository locally](SVNUsage.md) you can begin auto-building and testing the repo.  This script will update your repository to the latest version, then  generate a Clockworkmod flashable zip.

```
#! /bin/sh

#This is the repository Directory, change to match your setup
Repo="~/TeamKomin/trunk"
Output="~/Desktop"


svn update "$Repo"
test -e "$Output/tmp/" && rm -Rf "$Output/tmp/"
mkdir "$Output/tmp/"
cp -rf "$Repo/data" "$Output/tmp/"
cp -rf "$Repo/META-INF" "$Output/tmp/"
cp -rf "$Repo/system" "$Output/tmp/"
cp -rf "$Repo/updates" "$Output/tmp/"
find "$Output/tmp/" -name ".svn" -type d -exec rm -rf {} \;
cd "$Output/tmp"
test -e "$Output/AndromedaRepo.zip" && rm -f "$Output/AndromedaRepo.zip"
zip -r "$Output"/AndromedaRepo.zip ./*
rm -rf "$Output/tmp"
```



# Nightly builds #
Nightly Builds are generated automatically at 2AM. Any changes committed during the day will be reflected in the Nightly Builds.  The Nightly Builds are available here: http://code.google.com/p/teamkomin/downloads/detail?name=AndromedaNightly.zip&can=2&q=