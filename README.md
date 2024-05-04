# DRF_template
Django rest framework template set up with docker compose and a postgresql, database and custom user and admin

## Run management commands
Use docker compose to run django commands in docker-compose services:
```
docker-compose run --rm app sh -c "python manage.py <command-name>"
```

## Use with pycharm
Create a dummy venv from the requirements file and set pycharm to use it as python interpreter. This venv will not be used by the app, just for pycharm.
```
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
<set the .venv/bin/python as the python interpreter in pycharm>
```

**Note:** Pycharm should allow to use a python interpreter from docker-compose, but I didn't manage to do it. You can try.

## Configure dockerhub credentials

In dockerhub, log in, go to My Account > Security > New Access Token, and copy the created token.

Open the project created from this template in github, got to Settings > Secrets and variables > Actions, and add following repository secrets:

```
DOCKERHUB_TOKEN = <token-generated-in-dockerhub>>
DOCKERHUB_USER = <your-dockerhub-username>
```

