# NM Ansible

Ansible playbooks used to deploy nm-server and nm-web to production site

## nm-server
  - Installs build dependencies (nvm, node, yarn, pm2)
  - Checks out code from git repo to server
  - Builds code on server
  - Sets up nginx config
  - Restarts nginx and pm2 processes

## nm-web
  - Checkout scode from git repo locally
  - Builds code locally using webpack
  - Pushes code to server
  - Sets up nginx config
  - Restarts Server

