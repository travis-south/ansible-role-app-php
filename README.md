# Ansible Role: Server App

A role the provisions a web server with NGINX (or Apache) and PHP 7.

## Requirements

CentOS 7

## Role Variables

    use_nginx: yes
Possible values are `yes` and `no`. When `no` is selected, will install Apache instead. Default value is `yes`.

    front_controller: "app"
Possible values are `index` and `app` (for symfony apps). Default value is `app`.

    app_domain: "local-www.test.com"
Determines the domain of the app. Default value is `local-www.test.com`

    doc_root: "/var/www/html/app/web"
Determines the document root of your app. Default value is `/var/www/html/app/web`

## Dependencies

  - ansible-role-base-box
  - geerlingguy.repo-remi
  - geerlingguy.nginx
  - geerlingguy.php
  - geerlingguy.php-mysql
  - geerlingguy.apache
  - geerlingguy.apache-php-fpm


## Example Playbook
    - hosts: servers
      roles:
         - { role: ansible-role-server-app-php }

## License

MIT / BSD

## Author Information

Travis South