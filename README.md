# NM Ansible


Ansible playbooks used to deploy nm-server and nm-web to production site

## nm-server
```
ansible-playbook nm-server -e env=prod
```
  - Installs build dependencies (nvm, node, yarn, pm2)
  - Checks out code from git repo to server
  - Builds code on server
  - Sets up nginx config
  - Restarts nginx and pm2 processes


## nm-web
```
ansible-playbook nm-web -e env=prod
```
  - Checkout scode from git repo locally
  - Builds code locally using webpack
  - Pushes code to server
  - Sets up nginx config
  - Restarts Server

## Related Project
[nm-server](https://github.com/aaronstaves/nm-server) - backend server used to host [The TVDB API](https://api.thetvdb.com/swagger)

[nm-web](https://github.com/aaronstaves/nm-web) - frontend VueJS app used to access nm-server
