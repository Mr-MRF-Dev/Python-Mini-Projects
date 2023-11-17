# Python Clock Screen Saver

1. install tk and pyinstaller

    ```bash
    pip install tk
    pip install pyinstaller
    ```

2. clone code

    use [Git](https://git-scm.com/) on your system
   
    ```bash
    git clone https://github.com/Mr-MRF-Dev/python-mini-projects.git
    ```
    
    or use [GitHub CLI](https://cli.github.com/)

    ```bash
    gh repo clone Mr-MRF-Dev/python-mini-projects
    ```

3. The next step is to Change your directory.
    
    ```bash
    cd python-mini-projects/Clock-Screen-Saver
    ```

4. Create exe File

   ```bash
   pyinstaller --noconfirm --onefile --windowed  .\Clock-Screen-Saver.py
   ```

5. Change the file format to `scr`

    ```bash
    cd dist

    ren Clock-Screen-Saver.exe Clock-Screen-Saver.scr
    ```

6. move the file to `C:/windows/system32` (Administrator access is required)

    ```bash
    mv Clock-Screen-Saver.scr C:/windows/system32
    ```

7. install the new screen saver:

    ```bash
     reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v SCRNSAVE.EXE /t REG_SZ /d C:\Windows\system32\Clock-Screen-Saver.scr /f
    ```
    
    > reg add flags: `/v` \<Valuename\>, `/t` \<Type\>, `/d` \<Data\>, `/f` Adds the registry entry without prompting for confirmation.
    > [More about reg command](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/reg)

Done :)

## Tips:

- To see all screen savers:

    ```bash
    dir c:\windows\system32\*scr
    ```
    
- You can adjust the duration of the screen timeout (600 sec):

    ```bash
    reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v ScreenSaveTimeOut /t REG_SZ /d 600 /f
    ```
    
- Also, you don't need to rename the file to 'scr' extension. Instead, you can directly install the file with the 'exe' extension.

    ```bash
    reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v SCRNSAVE.EXE /t REG_SZ /d C:\Windows\system32\Clock-Screen-Saver.exe /f
    ```
