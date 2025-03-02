## Nsite-Upload

This repo is setup to be a small starter for deploying a static site as a Nsite using the Nsite-CLI.
In general this repo is setup to auto deploy using Github action but also can be used with the CLI to deploy from the terminal.

This is build on top of the work of some great folks: [Lez](https://github.com/lez) [flox1an](https://github.com/flox1an) [hzrd149](https://github.com/hzrd149)


### Getting Started Using this repository & Github Pages + Actions

##### 1) Clone this repo to your own github account or download it to your machine

#### 2) Edit the project.json file, ff you want to upload with a new Nsec you can by running the npx nsite-cli to start the dialogue.

##### Deploying from a new Nsec

If you have created your static website and want to deploy it using a fresh nsec you can utilise:

```
npx nsite-cli
```
without any subcommand, it will start an interactive dialog to set up a new project. 
Here you can also create a new private key (nsec) for signing, add custom relays and blossom servers. 
All settings will be saved in a .nsite/project.json file in the current working directory.


#### 3) Initial Deployment 'Use the CLI from your local machine this helps configure the required Blossom & Relay Servers. 

```
npx nsite-cli upload www
```

#### 4) To deploy using the github workflow set your the Nsec as a github secret to automate the deployment, 

! Nsec's are stored and used in hex format

##### Setting up a github Secret

https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-a-repository

NSITE_KEY = 'Nsec in hex'


#### 5) Configure your domain name

##### Setting a Apex domain at github pages

https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

