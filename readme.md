# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup

_Commands that are to be entered into a shell terminal are preceded by a `$`._ Lines that follow without a `$` represent the terminal output, which may differ slightly to your output based on the versions of the programs you have installed.

### Cloning the repo

Assuming you have [set up GitHub with an SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account):

```bash
$ git clone git@github.com:ObelusFamily/Anythink-Market-48abm.git
```

### Installing docker

Follow the instructions to [install Docker](https://docs.docker.com/get-docker/) on your local machine.

Check that you have successfully installed Docker with the following commands:

```bash
$ docker -v
Docker version 20.10.14, build a224086
```

```bash
$ docker-compose -v
docker-compose version 1.29.2, build 5becea4c
```

### Running the local dev environment

Run the following command to start the backend, frontend and database in local docker containers:

```bash
$ docker-compose up
# a lot of output...
```

To stop the local environment, press `Ctrl` + `C`.

### Manually test the application

To test the backend, either open http://localhost:3000/api/ping in your browser or send a GET request to that endpoint using `cURL` or a tool like [Postman](https://www.postman.com/).

To test the frontend and make sure it is connected to the backend, navigate to http://localhost:3001/register in your browser and register a new user.
