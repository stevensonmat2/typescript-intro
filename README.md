# CS 320

## TypeScript intro project

This is a sample project to help walk you through the development process that we'll be using for the assignments in this course. You'll install a couple necessary tools and learn how to read, run, and debug the kinds of programs that we'll be working with.

I recommend installing these tools on your own computer; they're all fully free and easy to uninstall after the course is over if you don't want them anymore. If you don't have a suitable computer to use, you may be able to get one on loan from the [PSU library](https://library.pdx.edu/study-spaces-computers/equipment), or you can use the Linux lab computers on campus.

Any text editor and web browser will be okay for working through the assignments in this course, but I'm only going to be providing instructions for compiling in VSCode or a terminal, and for debugging in VSCode and Firefox. If you're using a different editor or browser and you encounter problems, Katherine and I can try to help, but we can't make any guarantees.

### Installing Node.js

Node.js is a runtime environment for the V8 interpreter. We'll discuss more about what this means in lecture, but the very short version is that Node.js is like a virtual machine for running certain kinds of programs. The TypeScript compiler is designed to run within the Node.js virtual machine.

If you're working on the Linux lab computers, skip this step - they already have Node.js installed.

Open <https://nodejs.org> and click the link to download the LTS version for your operating system. Run the installer.

### Installing Firefox (optional, but recommended)

If you don't already have Firefox, I recommend installing it to use for debugging. Open <https://www.mozilla.org/en-US/firefox/download/thanks>, which should start the download automatically, and then run the installer.

### Installing Visual Studio Code (optional, but recommended)

Visual Studio Code (or VSCode) is a free open-source cross-platform development environment for TypeScript and many other languages. It is historically related to Microsoft's paid product called Visual Studio, but it's built from an entirely different codebase and offers a much more lightweight feature set.

If you don't already have a favorite development environment for programming, VSCode is a good one to start with, and it's especially well-suited for TypeScript. If you do already have a favorite environment, you can most likely find TypeScript plugins

Open <https://code.visualstudio.com> and download and run the installer.

Run VSCode; it should be in your start menu or apps list. If you're on a Unix-like system, the command name is `code`.

Open the "Extensions" tab in the left sidebar: the icon looks like four little squares with one square disconnected from the other three. Search "Debugger for Firefox" and click the "Install" button on the first result.

### Opening the project

Download the code of this sample project from <https://gitlab.cecs.pdx.edu/cas28/cs-320-spring-2022/-/archive/main/typescript-intro.zip>.

If you're using macOS or a GUI file manager on Linux, make sure to turn on the "show hidden files" setting in your file manager when you extract the zip archive. There should be a folder called ".vscode" in the archive, which will be invisible in your file manager by default because its name begins with a dot.

In VSCode, open the "File" menu and click "Open Folder..." if that option is there; otherwise click "Open". Either way, you should open the ***folder*** that you just extracted: the folder that contains `README.md`, `package.json`, etc. This is important: ***open the folder itself***, not any file ***in*** the folder. This is how VSCode knows where to find the project settings.

Alternatively, if you're working in a command line, navigate to this same folder in your terminal.

### Reading the code

The main source code file is `src/Main.ts`, which we'll explore and add some code to in lecture. It exposes a function called `main1`, which takes in two strings as input, prints each one to the browser developer console, and then updates the text of an element on the webpage.

### Building the project

You can compile the project from VSCode by opening the "Terminal" menu and choosing "Run Build Task..." and then "npm: build".

Alternatively, from a terminal in the project directory, you can compile by running the command `npm run build`.

You should see a folder called `build` appear in the project directory, with files named `compiled.js` and `compiled.js.map`. This is the compiled output of the code in `src/Main.ts`.

### Running the project

To run the project after building it, you can open the `html/index.html` file in a web browser. (Just drag the file onto the web browser application and it should open.)

You'll see two input boxes, which correspond to the `input1` and `input2` arguments to the `main1` function in `src/Main.ts`; a button, which runs the `main1` function with the given input; and an area for output, which is visually updated with the contents of `output.innerText` when `main1` runs.

### Debugging the project (requires VSCode and Firefox)

You can interactively debug the project in VSCode by opening the "Run" menu and choosing "Start Debugging". This will open a special Firefox window connected to VSCode.

To set a breakpoint, click to the left of a line number in VSCode and you should see a red dot appear. When execution reaches this line, the debugger will pause and let you inspect the state of the program.

Breakpoints can only be set on lines that have *runtime behavior*. In `src/Main.ts`, this is lines 6, 7, and 9.