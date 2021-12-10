# Pre-commit hooks with Python

This repo contains an example set-up for using pre-commit hooks with your python environment.

The file `.pre-commit-config.yaml` controls the type of pre-commit you are currently using. There exists [several](https://towardsdatascience.com/pre-commit-hooks-you-must-know-ff247f5feb7e) ways to do automatic formatting with Python. This is just an example.

## Usage
Activate the virtual environment

    sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pipenv shell

You can run `pre-commit` on all files with the command

    (pre-commit) sunnivin@NGI-R910LQ9W:~/NGI/pre-commit(main)$ pre-commit run --all-files


The set-up in this repositroy has been successfully tested with windows terminal for ubuntu-20.04 and windows power shell. 

Dependency:
- pipenv 
- pyenv 
- For windows: Microfost visual c++ 14.0 or greater 
