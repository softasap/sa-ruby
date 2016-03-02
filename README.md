sa-rubu
=========

* chruby
* ruby-install
* nginx + passenger
* sample application

Requirements
------------

Ubuntu 14.04 LTS

Role Variables
--------------

rubies_location: /opt/rubies
chruby_version: 0.3.9
ruby_install_version: 0.6.0
ruby_version: 2.3.0

option_install_app: false
option_install_nginx_passenger: true
option_ruby_install_setsystem: true


app_short_name: app
app_env: production
app_repository: https://github.com/RailsApps/rails-devise.git
app_base_dir: /var/www
app_www_root: "{{app_base_dir}}/public"

app_directories:
  - "{{app_base_dir}}"




Example Playbook
----------------

- hosts: www

  vars:
    - root_dir: ..


  pre_tasks:
    - debug: msg="Pre tasks section"

  roles:
     - {
         role: "sa-ruby",
         ruby_install_setsystem: true,
         ruby_version: 2.3.0,

         option_install_sampleapp: false,
         option_install_nginx_passenger: true
       }

  tasks:
    - debug: msg="Tasks section"


License
-------

MIT

Author Information
------------------

http://www.softasap.com/
