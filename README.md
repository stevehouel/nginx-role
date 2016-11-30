# Nginx Creation role #


## Requirements

This project must be cloned under specific project's Ansible Roles to Create Nginx Container.

## Mandatory Variables

`nginx_version` : Docker Nginx image version

## Optional Variables

`nginx_path` : Nginx Root Path for configurations and certificates. Default to */data/nginx*

`nginx_certs_path` : Nginx Certs Path. Default to *"{{ nginx_path }}/certs"*

`nginx_htpasswd_path` : Nginx HtPasswd Path. Default to *"{{ nginx_path }}/htpasswd"*

`nginx_config_path` : Nginx Config Path. Default to *"{{ nginx_path }}/config"*

`nginx_port` : Listen port HTTP on Docker host to map to nginx container. Default to *800*

`nginx_https_port` : Listen port HTTPS on Docker host to map to nginx container. Default to *4430*

`athena_registry_url` : Url of the Registry used to pull images. Default to *registry.prod.athena.ts-agora.com/athena*

`nginx_container_name` : Container's name. Defaults to *nginx*

## Files

* You CAN create a folder with path `conf-nginx/certs` to include certificates files for the nginx servers.
* You CAN create a folder with path `conf-nginx/htaccess` to include .htaccess files for the nginx servers.

* You NEED TO create a file with path `conf-nginx/config/proxy.conf` to include nginx extra configurations.
