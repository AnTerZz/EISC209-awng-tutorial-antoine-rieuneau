# Antoine Rieuneau


# Empty project to follow the Django 4 official tutorial

Note: this project contains a `.gitignore` file, so that you will only share *source* code on GitHub. In particular it ignores:

- Compiled Python code (`.pyc` files)
- VS Code IDE stuff (`.vscode/` subdir)
- SQLite database content (`db.sqlite3` file)
- etc.

## Get your own local copy of this project

1. Fork this project:
   1. Click the "Fork" button in the-top right corner of this page
   2. Select your GitHub account; you will be landing in *your* project's GitHub page (`john-doe/awng-tutorial` instead of `EISC-209-AWNG/awng-tutorial`)
2. Add your teachers as members of ***your*** project:
   1. Go to Settings / Collaborators on your project's GitHub page
   2. Use Add Collaborator for each teacher (type its GitHub identifier) :
      - `brunoilponseisae`
      - `tanguy-perennou`
      - `trsalomon`
3. Allow teachers to create issues in your project
   1. Go to Settings / General on your project's GitHub page
   2. Scroll down until you find the Features section, and enable the Issues feature
4. Rename your project so that it clearly identifies you:
   1. Go to Settings/ General on your project's GitHub page
   2. Type the new Repository Name: `awng-tutorial-firstname-lastname`, with *your* name, e.g. `awng-tutorial-john-doe`
   3. Click the "Rename" button

At this point, you have your own project on GitHub with an appropriate initial content. Next, you need to get a **working copy** on your computer:

1. Follow the instructions of the [*Cloning your forked repository*](https://docs.github.com/en/get-started/quickstart/fork-a-repo#cloning-your-forked-repository) section of <https://docs.github.com/en/get-started/quickstart/fork-a-repo>
2. Launch VS Code and open the local directory, named `awng-tutorial-firstname-lastname`
3. In your local project directory, create a virtual environment and install Django (see next section)

## Install Django in a virtual environment

The following commands create a `venv` virtual environment in your local copy of the project, and let you install `Django` inside this virtual environment; you will also install the `djlint` tool that VS Code uses to detect some syntax errors. Those installs are made with the `pip` command which is part of the Python distribution.

Open a terminal in your local directory (it can be VS Code integrated terminal), and type the following commands (after the `$` prompt sign); notice the `(venv)` prompt prefix, which indicates when you are in the virtual environment:

### On Linux or macOS

```bash
$ cd /path/to/project
$ python -m venv venv
$ source venv/bin/activate
(venv) $ pip install Django
(venv) $ pip install djlint
```

### On Windows via Git Bash

```bash
$ cd /path/to/project
$ py -m venv venv
$ source venv/Scripts/activate
(venv) $ pip install Django
(venv) $ pip install djlint
```

### On Windows via powershell

```powershell
$ cd \path\to\project
$ py -m venv venv
$ venv\Scripts\activate
(venv) $ pip install Django
(venv) $ pip install djlint
```

Warning: `activate` might not work on Windows, complaining about some "execution policy" matter. In that case, open a powershell console, run `Set-ExecutionPolicy -scope CurrentUser` and answer `bypass`.

## Use the virtual environment afterwards

Every time you will use a *new* terminal/console to type python or Django commands, you will need to reactivate the virtual environment by calling the `activate` script. Actually, you need to run the `activate` script if you do not see `(venv)` before the shell prompt.

For instance, every time you restart VS Code to work on the project, you will have to go to the project local directory if needed, and then to activate `venv`:

```bash
$ cd /path/to/project
$ source venv/bin/activate
(venv) $ 
```

or on Windows via powershell in VS Code:

```powershell
$ cd \path\to\project
$ venv\Scripts\activate
(venv) $ 
```

or on Windows via Git Bash in VS Code:

```bash
$ cd /path/to/project
$ source venv/Scripts/activate
(venv) $ 
```

## Do the Django official tutorial in VS Code

Open the `/path/to/project` folder in VS Code (menu File > Open Folder...). Your
VS Code should already be configured with Python, Django and SQLite3 extensions
according to previous instructions.

Then open [*Django's Getting Started
documentation*](https://docs.djangoproject.com/en/4.1/intro/) and do the seven
parts of the **Writing your first Django app** tutorial, which consists in
coding a `mysite/polls` Django web server.

### Regularly save your work with Git

- First, to your local copy, with regular and frequent calls to `git add ...`
  and `git commit -m "..."`
- Also, to your GitHub repository, with regular calls to `git push`
- If in doubt, use `git status` and `git log`

:warning: Focus on commits quality:

- Every commit should be **atomic**: consistent set of modifications, tested and
  validated.
- Every commit must also be **documented**: provide a comment which is useful to
  you as well as other readers: what did you do between the commit and the
  previous one? Here are a few examples: "Add Choice model", "Add index view
  plus associated URL", "Django tutorial part 3". These messages must inform you,
  even after 3 months.

:bulb: When you are comfortable with `git add` and `git commit`, systematically
use a new **branch** for each new tutorial chapter (see Git slides on LMS). You
will then use `git branch`, `git switch` and `git merge`.

## Read extra resources

- [*Working with forms*](https://docs.djangoproject.com/en/4.1/topics/forms/)
- [*How to manage static files (e.g. images, JavaScript, CSS)*](https://docs.djangoproject.com/en/4.1/howto/static-files/)
- [*The Django template language*](https://docs.djangoproject.com/en/4.1/ref/templates/language/#template-inheritance-1)
