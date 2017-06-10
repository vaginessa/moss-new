Moss
====

Moss is a [Conky][conky] like live wallpaper for android. It provides system statistics
such as uptime, cpu usage, network usage, top processes, and battery level.
It is highly configurable. Configuration tries to closely follow [Conky's][conky] syntax. 

For example configurations please see [the samples on the Moss site][samples].

# Build from Command Line

Be sure you have jdk1.7, android-ndk-r10 and android-sdk SDK 21 and 21.0.+ build tools.

    # Sorry about the submodules
    git submodule init && git submodule update

    # build and install
    ./gradlew installDebug

[conky]: http://www.conky.com
[samples]: http://teneighty.github.com/moss/samples.html

Some modifications by ohnonot:  
had to edit some files to make it compile on my system (archlinux, june 2017).  
Then I added my custom configuration (Ming Configuration).
Because on phone bootup, moss would not load an installed patch from the sdcard.  
I also removed one line of code that would draw a box around graphs; a feature i find ugly.  
most changes are likely specific to my setup (computer AND phone), but of course you're free to try.

list of files originally changed in first commit:

	modified:   build.gradle
	modified:   gradle.properties
	modified:   gradle/wrapper/gradle-wrapper.properties
	new file:   moss/src/main/assets/ming.conf
	modified:   moss/src/main/java/org/mosspaper/PackageDatabase.java
	modified:   moss/src/main/java/org/mosspaper/util/Graph.java
	modified:   moss/src/main/res/values/arrays.xml
	modified:   moss/src/main/res/values/strings.xml
