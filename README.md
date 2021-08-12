A playbook which has the following roles :
- Docker :
    - Installed after adding the docker-repo to yum_repository using which Docker CE is installed.
    - After this, a handler would start the docker engine.
- Nginx :
    - Installls epel-release and then it installs nginx.
    - The nginx.conf template is copied to /etc/nginx/nginx.conf which would overrides the existing configuration.
    - Finally, a handler would start/relaod the nginx based upon the task
- Logrotate :
    - Logrotate is installed and the template for nginx logs is coped to /etc/logrotate.d/nginx with required rules.