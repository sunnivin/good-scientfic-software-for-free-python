# Pre-commit hooks with Python

This repo contains an example set-up for using pre-commit hooks with your python environment.

The file `.pre-commit-config.yaml` controls the type of pre-commit you are currently using. There exists [several](https://towardsdatascience.com/pre-commit-hooks-you-must-know-ff247f5feb7e) ways to do automatic formatting with Python. This is just an example.

## Usage

Activate the virtual environment

```
sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pipenv shell
```

You can run `pre-commit` on all files with the command

```
(pre-commit) sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pre-commit run --all-files
```

The set-up in this repositroy has been successfully tested with windows terminal for ubuntu-20.04 and windows power shell 7.

### Usage on windows: 
On Windws `pipenv shell` could spawn CMD. If CMD is not your perferred terminal you can fix this error by setting an environmental variable called `PIPENV_SHELL`
```
$Env:PIPENV_SHELL = "powershell"
```
Read more about why [here](https://github.com/pypa/pipenv/issues/4264).

## Dependencies:
- pipenv
- pyenv
    - For windows: Microsoft visual c++ 14.0 or greater
    - PowerShell 7 