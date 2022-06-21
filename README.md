# Pre-commit hooks with Python

This repo contains an example set-up for using pre-commit hooks with your python environment.

The file `.pre-commit-config.yaml` controls the type of pre-commit you are currently using. There exists [several](https://towardsdatascience.com/pre-commit-hooks-you-must-know-ff247f5feb7e) ways to do automatic formatting with Python. This is just an example.

Original documentation for [pre-commit](https://pre-commit.com/).

## Usage

Start with activating the virtual environment and installing needed packages from the `Pipfile` and `Pipefile.lock`

```
sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pipenv shell
(pre-commits-python-example)sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pipenv install
```

### Automatic run each time you try to commit something
```
(pre-commits-python-example)sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pre-commit install
```
To later bypass the hook use the `--no-verify` option
```
(pre-commits-python-example)sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ git commit -m "wip: quick fix of data" --no-verify
```

### Manual run
You can do a manual `pre-commit` run on all files with the command
```
(pre-commits-python-example)sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pre-commit run --all-files
```



### Usage on windows:

#### PowerShell 5.2
On Windws `pipenv shell` could spawn CMD. If CMD is not your perferred terminal you can fix this error by setting an environmental variable called `PIPENV_SHELL`
```
$Env:PIPENV_SHELL = "powershell"
```
Read more about why [here](https://github.com/pypa/pipenv/issues/4264).

#### PowerShell 7.2.1
Run `pipenv run pwsh` instead of running `pipenv shell` to start a virtual environment.


## Dependencies:
- pipenv
- pyenv
- For windows 10:
    -Microsoft visual c++ 14.0 or greater

## Tested on
Works successfully on
- WSL2, Ubuntu 20.04
- PowerShell 5.2
- PowerShell 7.2.1
- cmd
