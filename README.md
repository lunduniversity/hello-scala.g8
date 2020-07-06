# hello-scala.g8
A [Gitter8](http://www.foundweekends.org/giter8/index.html) template for a minimal Scala project with a minimal build file.

## Usage

You need to have Scala tools installed as described in the "Preparations" section below. Then you can use this template within VS Code with Scala (Metals) or in terminal as follows.

### In VS Code with Scala (Metals)

* Click the curly metals *m* logo in the left bar
* Click "New Scala Project" under BUILD COMMANDS
* Scroll down and select "**Custom** *Enter template manually*"
* Enter `lunduniversity/hello-scala.g8` and press enter 
* Click on "Ok"
* Confirm again with Enter
* Select "Yes" when asked to open in new window
* In new window, wait for stuff to download and start and then click the button **Import** when question if *import build* comes up in the lower right corner.
* Open the file called `Main.scala` and press *run* in the "run | debug" field just above the `def main` line. 

### In terminal
Copy-paste or type each line at a time followed by enter, after waiting for each command to finnish:
```
sbt new lunduniversity/hello-scala.g8
cd hello-scala
sbt
run
```

## Preparations

### Install Scala tools:
  * **Windows**: open powershell and copy-paste these two lines, one line at a time followed by enter:
    ```
    bitsadmin /transfer cs-cli https://git.io/coursier-cli-windows-exe "%cd%\cs.exe"
    .\cs setup
    ``` 
  * **MacOS**: open terminal and copy-paste this in one line and press enter:
    ```
    curl -fLo cs https://git.io/coursier-cli-macos && chmod +x cs && (xattr -d com.apple.quarantine cs || true) &&
      ./cs setup
    ```
  * **Linux**: open terminal (Ctrl+Alt+T) and copy-paste this in one line and press enter:
    ```
    wget -O cs https://git.io/coursier-cli-linux && chmod +x cs && ./cs setup
    ```
### Install VS Code 
  * Install from here: https://code.visualstudio.com/download
  * ...then inside VS Code install the extension called **Scala (Metals)** by selecting menu *View -> Extensions* or pressing Ctrl+Shift+X and search by typing `metals` in the search field, select **Scala (Metals)** and click the green *install* button.