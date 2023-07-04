# github-ci
Lets explains what each of the lines does

name: CI

This is just specifying a name for the workflow

on: [push]

The on command is used to specify an event that will trigger the workflow, this event can be push, pull_request, etc. It can also be an array of events like this.

# Use an array when using more than one event
on: [push, pull_request] 
In our case, we are simply saying trigger this workflow on every push

jobs:

Here we are specifying the job we want to run, in this case, we are setting up a build job.

runs-on: ubuntu-latest

The runs-on is specifying the OS you want your workflow to run on and we are using the latest version of ubuntu

Steps:

Steps just indicate the various steps you want to run on that job

uses: actions/checkout@v1

Github has some already define Actions, we are using version 1 of the checkout action this is responsible for cloning the repo and checking into our project directory.

The other steps just show how to run one or more commands in the shell. the default shell is bash.
