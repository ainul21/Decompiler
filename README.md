## Decoding .APK Files - Step-by-Step Guide

Follow these steps to decode .apk files and access the source code:

### Step 1: Rename and Extract .APK

1. Create a new folder and copy the .apk file you want to decode into it.
2. Rename the .apk file's extension to .zip (e.g., rename `filename.apk` to `filename.zip`) and save it.
3. Now, you can access the `classes.dex` files. You'll be able to see drawables but not .xml and .java files.

### Step 2: Extract .dex File

1. Extract the contents of the .zip file you renamed in the same folder or a new folder.
2. Download `dex2jar` from [here](https://github.com/pxb1988/dex2jar/releases) (choose the ZIP file under Releases) and extract it to the same folder.
3. Move the `classes.dex` file into the `dex2jar` folder.
4. Open Command Prompt and navigate to that folder.
5. Run the command `d2j-dex2jar classes.dex` (for Mac or Ubuntu, use `./d2j-dex2jar.sh classes.dex`) and press Enter. You will now have a `classes.dex.dex2jar` file in the same folder.
6. Download a Java decompiler such as JD-GUI, right-click on it, select "Open File," and open `classes.dex.dex2jar` from the folder. You will get the class files.
7. Save all of these class files by selecting "File -> Save All Sources" in JD-GUI. You will have the Java code at this stage, but the .xml files are still unreadable.

### Step 3: Decode .APK Resources

1. Create a new folder.
2. Put the .apk file you want to decode into this new folder.
3. Download the latest version of `apktool` and `apktool` install from [here](https://github.com/iBotPeaches/Apktool/releases) and place them in the same folder.
4. Open the Command Prompt.
5. Run the command `apktool if framework-res.apk` (if you don't have it, download it) and then `apktool d myApp.apk` (replace `myApp.apk` with your filename).
6. You will now get a file folder in the folder containing decoded .xml files.

### Step 4: Combine Contents

It's not a specific step, but you can copy the contents of both new folders into a single folder.

Enjoy exploring the source code!


https://stackoverflow.com/questions/3593420/is-there-a-way-to-get-the-source-code-from-an-apk-file#:~:text=Simplest%20way%3A%20use%20the%20online%20tool%20Decompiler%2C,upload%20the%20apk%20and%20get%20the%20source%20code.