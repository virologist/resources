# PAML & Treesub

*Written by: Don Teng<br>
Last update: 15 June 2017<br>*

## [PAML](http://abacus.gene.ucl.ac.uk/software/paml.html)
...stands for *Phylogenetic Analysis by ML*. It has several uses, such as inferring ancestral sequences based on modern sequences. 

### Installation
This is actually quite easy, but you're encouraged to get 2 versions:
1. The point-and-click interface. Either download and install it as a normal bit of software, or use `brew install`. 
2. The executable file, which `treesub` requires. This isn't the download link at the top of the `PAML` site (that's the GUI), it's hidden somewhere in the middle.  Ctrl-F "For the MAC, we have compiled a version for MAC OSX". 

## Run
(I've never run this before, so WIP).

## [Treesub](https://github.com/tamuri/treesub)
This is an extension which uses some `PAML` functions, stitched together with RAXML and FigTree. It's primarily useful for producing a tree which shows the amino acid substitutions along the branches. 

### Installation

The repo hasn't been updated in a while, so the installation instructions are slightly out of date. Unfortunately, the bits which are out of date are precisely those bits which are the hardest to install. 

You'll need to get:
1. RAxML (Not easy. See the *RAXML installation tutorial*)
2. PAML executable
3. The latest Java SDK version, which is currently 8. Get it [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
4. FigTree (easy)
5. The [Eclipse](https://www.eclipse.org/downloads/?) IDE, which is not actually used by `treesub`; you need it to get a `treesub.jar` application.

**Procedure**
1. Open Eclipse, and open `build.xml` from inside the `treesub` folder.
2. Run the file, either from the taskbar at the top of the window (look for the button that has a "play" icon on it), or select Run > Run from the toolbar at the top. You should see some output being printed out like:

```
Buildfile: /Users/dten0001/Documents/clones/treesub/build.xml
clean:
makedir:
    [mkdir] Created dir: /Users/dten0001/Documents/clones/treesub/build
    [mkdir] Created dir: /Users/dten0001/Documents/clones/treesub/docs/api
    [mkdir] Created dir: /Users/dten0001/Documents/clones/treesub/dist
compile:
    [javac] /Users/dten0001/Documents/clones/treesub/build.xml:29: warning: 'includeantruntime' was not set, defaulting to build.sysclasspath=last; set to false for repeatable builds
    [javac] Compiling 8 source files to /Users/dten0001/Documents/clones/treesub/build
    [javac] Note: /Users/dten0001/Documents/clones/treesub/src/treesub/gui/AnnotatorGUI.java uses or overrides a deprecated API.
    [javac] Note: Recompile with -Xlint:deprecation for details.
jar:
      [jar] Building jar: /Users/dten0001/Documents/clones/treesub/dist/treesub.jar
dist:
BUILD SUCCESSFUL
Total time: 1 second
```

3. This will create a `treesub.jar` executable, which you can launch the point-and-click interface from. This will be inside `.../treesub/dist/treesub.jar`.

For those familiar with Java, my guess is that this is a Java file that needs to be locally compiled.

### Run
1. Double-click on the `treesub.jar` file to launch it, like you would a normal application. 
2. Fill in the fields where you installed the `RAXML` and `PAML` executables. `PAML` comes with a lot of files; look for `/paml<version number>/bin/baseml`.

The rest of the run instructions are on the `treesub` repo itself. 