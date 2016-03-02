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
ruby_install_setsystem: true
ruby_version: 2.3.0



app_short_name: app
app_env: production
app_repository: https://github.com/RailsApps/rails-devise.git
app_base_dir: /var/www
app_www_root: "{{app_base_dir}}/public"

app_directories:
  - "{{app_base_dir}}"




Example Playbook
----------------


License
-------

MIT

Author Information
------------------

http://www.softasap.com/
