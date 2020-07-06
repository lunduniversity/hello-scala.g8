# hello-scala.g8
A [Gitter8](http://www.foundweekends.org/giter8/index.html) template for a minimal Scala project with a minimal build file.

## Usage

You need to have Scala tools installed as described in the "Preparations" section below. Then you can use this template in terminal or within VS Code with Scala (Metals), as follows.

### In terminal
Copy-paste or type each line at a time followed by enter, after waiting for each command to finnish:
```
sbt new lunduniversity/hello-scala.g8
cd hello-scala
sbt
run
```

### In [VS Code](https://code.visualstudio.com/download) with [Scala (Metals)](https://scalameta.org/metals/docs/editors/vscode.html#installation)

* Click the curly metals *m* logo in the left bar
* Click "New Scala Project" under BUILD COMMANDS
* Scroll down almost to the bottom and select "**Custom** *Enter template manually*"
* Type `lunduniversity/hello-scala.g8` and press enter 
* Click on "Ok"
* Confirm again with Enter
* Select "Yes" when asked to open in new window
* In new window, wait for stuff to download and start and then click the button **Import** when question if *import build* comes up in the lower right corner.
* Open the file called `Main.scala` and press *run* in the "run | debug" field just above the `def main` line. 


## Preparations: install Scala tools

1. Install **OpenJDK 11** for your platform from https://adoptopenjdk.net/

2. Install the **Scala** programming language
     - Windows: https://downloads.lightbend.com/scala/2.13.3/scala-2.13.3.msi
     - Linux: https://downloads.lightbend.com/scala/2.13.3/scala-2.13.3.deb
     - Mac: use [Homebrew](https://brew.sh/) by pasting in Terminal:
       ```
       /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
       brew update
       brew install scala
       ```
3. Install the Scala build tool **sbt**  
      - Windows: https://piccolo.link/sbt-1.3.13.msi
      - Mac: 
        ```
        brew install sbt
        ``` 
4. Install VS Code from here: https://code.visualstudio.com/download

5. From inside VS Code install the extension called **Scala (Metals)** by selecting menu *View -> Extensions* or pressing Ctrl+Shift+X and search by typing `metals` in the search field, select **Scala (Metals)** and click the green *install* button.

#### Alternative method to install jdk, scala, sbt: use coursier
The commands below are adopted from https://get-coursier.io/docs/cli-installation

  * **Linux**: open Terminal (Ctrl+Alt+T) and copy-paste this in one line and press enter:
    ```
    wget -O cs https://git.io/coursier-cli-linux && chmod +x cs && ./cs setup
    ```
    Logout from this session and login again (or reboot) and after that you should be able to start the Scala REPL by typing `scala` in a terminal window.

  * **Windows**: *[this did not work for windows at the time of writing, as JAVA_HOME was not set properly and did not install JDK 11]* open a cmd-terminal (press windows-key and type `cmd` and press Enter) and copy-paste these two lines, one line at a time, each followed by pressing Enter:
    ```
    bitsadmin /transfer cs-cli https://git.io/coursier-cli-windows-exe "%cd%\cs.exe"
    cs setup
    cs update
    ``` 
    Type `Y` as answer to questions that you get. When everything is installed, **reboot** your computer and then you should be able to start the Scala REPL by typing `scala` in a powershell window.

  * **MacOS**: *[this did not install JDK 11 but old JDK 8]* open Terminal (click magnifyer and search for Terminal) and copy-paste this in one line and press enter:
    ```
    curl -fLo cs https://git.io/coursier-cli-macos && chmod +x cs && (xattr -d com.apple.quarantine cs || true) &&
      ./cs setup
    ```
    Type `Y` as answer to questions that you get.
    When everything is installed, quit this terminal window an open a new terminal window (Command+N) and in that new terminal window type `scala` end press enter check if you now can start the Scala REPL. 

