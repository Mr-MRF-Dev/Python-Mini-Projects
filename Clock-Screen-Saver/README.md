# Python Clock Screen Saver

- install tk and pyinstaller

```bash
pip install tk
pip install pyinstaller
```

- clone code

```bash
# use git on your system
git clone https://github.com/Mr-MRF-Dev/python-mini-projects.git

# or use github CLI
gh repo clone Mr-MRF-Dev/python-mini-projects

cd python-mini-projects/Clock-Screen-Saver
```

- Create exe File

```bash
pyinstaller --noconfirm --onefile --windowed  .\Clock-Screen-Saver.py
```

- Change the file format to `scr`

```bash
cd dist

ren Clock-Screen-Saver.exe Clock-Screen-Saver.scr
```

- Open the folder with the explorer

```bash
explorer .
```

- NOW Right click on the final file and click `install` : )
