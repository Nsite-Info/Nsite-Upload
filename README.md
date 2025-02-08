## Nsite

This repo is setup to be a small starter for deploying a already static site as a Nsite.
It will also be a small TODO & Tracker on things i'd like to build on top of the Nsite Concept.

In general this repo is setup to auto deploy using Github action but also can be used with the CLI to deploy from the terminal.
But first things first: this is build using the work of some great folks: [Lez](https://github.com/lez) [flox1an](https://github.com/flox1an) [hzrd149](https://github.com/hzrd149)


### Getting Started Using this repository & Github Pages + Actions

0) Clone this repo to your own github account or download it to your machine

1) Remove the project.json file 
If you want to upload with a new Nsec you can by running the npx nsite-cli to start the dialogue.

2) Initial Deployment 'Use the CLI local this helps configure the required Blossom & Relay Servers 
( it might be required to disable the publish profile. )

Command:    npx nsite-cli upload www

3) Setup the Nsec to automate the deployment

4) Configure your domain name


! Nsec's are stored and used in hex format

## TODO Tracker

[ ] Simple Website 
[ ] Github Action
[ ] Nsite Resolver ( Single Homepage ) + Document custom domain 
[ ] Create Nsite Hopeage Resolver ( Docker Container with Nginx )
[ ] Nsite Resolver ( Public for multiple sites )
[ ] Simple IDE that loads existing Nsite for editing 
[ ] Setup for NuxtJS ( Port Over Cypher)


## Procedures

#### Deploying from a new Nsec

If you have created your static website and want to deploy it using a fresh nsec you can utilise:

 run npx nsite-cli without any subcommand, it will start an interactive dialog to set up a new project. Here you can also create a new private key (nsec) for signing, add custom relays and blossom servers. All settings will be saved in a .nsite/project.json file in the current working directory.

#### Setting a Apex domain at github pages

https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

#### Setting up a github Secret

https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-a-repository

NSITE_KEY = 'Nsec in hex'


#### Local Upload 

From the command line run npx nsite-cli to upload the website, it will use the nsec, relays and blossom servers that are stored in the .nsite / project.json folder.