A clean, repeatable setup process for running any Python project safely using a virtual environment — without polluting your repo or system.

---

## 1. Create a Virtual Environment (Outside Repo)

Create it once, in your home directory:
```bash
cd ~
python3 -m venv venv-projectname
```

Activate it:
```bash
source ~/venv-[project-name]/bin/activate
```

When activated, your prompt will look like:
```bash
(venv-projectname) user@machine:~$
```
## 2. Clone GitHub Repository

Keep code in a separate folder (not inside the venv):
```bash
cd ~/Projects
git clone https://github.com/username/repo-name.git
cd repo-name
```
## 3. Install Dependencies

If project has a requirements.txt:
```bash
pip install -r requirements.txt
```

If not:
```bash
pip install [dependencies]

e.g. pip install pygame
```
## 4. Configure VS Code to Use Virtual Environment

1. Open project in VS Code:
```bash
code .
```

2. Press Ctrl + Shift + P -> select:
```vbnet
Python: Select Interpreter
```

3. Choose:
```
~/venv-[project-name]/bin/python
```

4. Open a new terminal in VS Code and verify:
```bash
which python
```
Output should be:
```
/home/[user]/[venv-project-name]/bin/python
```

Should now be able to run the program
## 5. Optional: Create/Update .gitignore

Inside project folder, add/update .gitignore file:
```gitignore
# Virtual environments
venv/
env/
__pycache__/
*.pyc
*.pyo
*.pyd
```
