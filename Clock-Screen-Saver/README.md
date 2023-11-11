# Python Clock Screen Saver

1. install tk and pyinstaller

    ```bash
    pip install tk
    pip install pyinstaller
    ```

2. clone code

    ```bash
    # use git on your system
    git clone https://github.com/Mr-MRF-Dev/python-mini-projects.git

    # or use github CLI
    gh repo clone Mr-MRF-Dev/python-mini-projects

    cd python-mini-projects/Clock-Screen-Saver
    ```

3. Create exe File

   ```bash
   pyinstaller --noconfirm --onefile --windowed  .\Clock-Screen-Saver.py
   ```

4. Change the file format to `scr`

    ```bash
    cd dist

    ren Clock-Screen-Saver.exe Clock-Screen-Saver.scr
    ```

5. move file to `C:/windows/system32`

    ```bash
    mv Clock-Screen-Saver.scr C:/windows/system32
    ```

6. install the new screen saver:

    ```bash
     reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v SCRNSAVE.EXE /t REG_SZ /d C:\Windows\system32\Clock-Screen-Saver.scr /f
    ```

Done :)

## Tips:

- To see all screen savers:

    ```bash
    dir c:\windows\system32\*scr
    ```
    
- You can adjust the duration of the screen timeout:

    ```bash
    reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v ScreenSaveTimeOut /t REG_SZ /d 600 /f
    ```
    
- Also, you don't need to rename the file to 'scr' extension. Instead, you can directly install the file with 'exe' extension.

    ```bash
    reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v SCRNSAVE.EXE /t REG_SZ /d C:\Windows\system32\Clock-Screen-Saver.exe /f
    ```
