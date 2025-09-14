# zeropkg
A super minimal shell script (POSIX) based package manager written in under 2 days, 
its under 130 lines of code and still is (kind of) useable
## features
- Installing a package from a gzip archive
- Using curl to get an archive (or any file) from a url
- Removing a package
- Purging a package (remove but deletes anything related to it)
- A nice modern usage message (not important but it looks nice haha)
- Viewing package metadata (eg name and description, its all defined in a metadata.txt file in the package archive)
- Listing installed packages
- It can also generate a default config file (you would first create an empty file at /etc/zeropkg.cfg)
## why did i make it
boredom and experience, i wanted to get better at shell scripting and i thought a package manager
would be a pretty cool thing, its semi inspired by the kiss package manager because i enjoy using it
## usage
- ```zeropkg -i example.tar.gz``` this would run a build script (more of an install script) copy a remove script used to remove the package, 
metadata.txt for metadata and a name file for getting the package name (so you can remove it etc)
- ```zeropkg -r example``` this would run the previously copied remove script and remove the package
## how can i port packages? (if you really want to)
a zeropkg package must be compressed in a tar.gz format and contain a build script (for installing ik the name is misleading) a remove script
for removing your package and a metadata.txt script for a name description or whatever you want to add it is just a .txt file and a name file
which contains the name of your package (because im too lazy to figure out how to get it out of metadata.txt)
## installing zeropkg
installing zeropkg is actually quite simple!
- clone the repository: `git clone https://github.com/v1nch3ns0/zeropkg`
- make the script executable: `chmod +x zeropkg`
- copy the example or generate a config: `sudo touch /etc/zeropkg && zeropkg -g` or `cp zeropkg.cfg /etc/zeropkg.cfg`
- move the script to somewhere in PATH eg /usr/bin: `sudo mv zeropkg /usr/bin/`
and thats it! pretty short ig haha
