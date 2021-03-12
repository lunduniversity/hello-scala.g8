# hello-scala.g8
A [Gitter8](http://www.foundweekends.org/giter8/index.html) template for a minimal Scala project with a minimal build file.

## Usage

You need to have Scala tools installed as described in the [Preparations](https://github.com/lunduniversity/hello-scala.g8#preparations-install-scala-tools) section below. Then you can use this template in terminal or within VS Code with Scala (Metals), as follows.

### How to use this template in terminal:
Type this in terminal to create a scala project:
```
sbt new lunduniversity/hello-scala.g8
```
Wait a while. After a while the template has been downloaded from github and you are prompted to give a name for your scala project. The output looks something like this:
```
$ sbt new lunduniversity/hello-scala.g8
[info] Loading settings for project global-plugins from gpg.sbt ...
[info] Loading global plugins from /home/bjornr/.sbt/1.0/plugins
[info] Loading project definition from /home/bjornr/tmp/project
[info] Loading settings for project tmp from build.sbt ...
[info] Set current project to tmp (in build file:/home/bjornr/tmp/)
[info] Set current project to tmp (in build file:/home/bjornr/tmp/)

Minimal Scala app with minimal build file 

name [hello]: myProjectName

Template applied in /home/bjornr/tmp/./myProjectName
$
```
Now you can navigate to a folder with the name you gave the project and start sbt and run your Scala app by typing these commands:
```
cd myProjectName
sbt
run
```

### How to use this template in [VS `code`](https://code.visualstudio.com/download) with [metals](https://marketplace.visualstudio.com/items?itemName=scalameta.metals)

* Click the curly metals *m* logo in the left bar
* Click "New Scala Project" under BUILD COMMANDS
* Scroll down almost to the bottom and select "**Custom** *Enter template manually*"
* Type `lunduniversity/hello-scala.g8` and press enter 
* Click on "Ok"
* Confirm again with Enter
* Select "Yes" when asked to open in new window
* In new window, wait for stuff to download and start and then click the button **Import** when question if *import build* comes up in the lower right corner.
* Open the file called `main.scala` and press *run* in the "run | debug" field just above the `def run` line. 


## Preparations: install `jdk`, `sbt`, VS `code`

1. Install **OpenJDK 11** for your platform from https://adoptopenjdk.net/

2. Install the Scala build tool **sbt**  
      - Windows: https://github.com/sbt/sbt/releases/download/v1.4.8/sbt-1.4.8.msi
      - Linux: https://www.scala-sbt.org/download.html
      - Mac: (skip the first command below if you already have homebrew installed)
        ```
        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
        brew install sbt
        ``` 
3. Install VS `code` from here: https://code.visualstudio.com/download

4. From inside VS `code` install the extension "metals" as described here: https://marketplace.visualstudio.com/items?itemName=scalameta.metals



