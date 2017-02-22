# Ansible role PHP-fpm

Version: 0.0.1

Supported OS: Ubuntu

Ansible role PHP-fpm

## Role variables
```
php_fpm_main_packages: [ 'php7.0-fpm', 'php7.0-cli' ]
php_fpm_additional_packages: []

php_fpm_process_name: php7.0-fpm

php_fpm_pools: []

# Example PHP-FPM pool, explanation of variables can be found
# in templates/etc/php7.0/fpm/pool.d/pool.conf.j2
#php_fpm_example_pool:
  #name: 'www-data'  # Mandatory

  #prefix: ''

  #user: 'www-data'
  #group: 'www-data'

  #listen: '/var/run/php7.0-fpm-www-data.sock'

  #environment:
  #  HOSTNAME: '$HOSTNAME'
  #  PATH: '/usr/local/bin:/usr/bin:/bin'
  #  TMP: '/tmp'
  #  TMPDIR: '/tmp'
  #  TEMP: '/tmp'

  #php_flag:
  #  display_errors: 'off'

  #php_value:
  #  default_mimetype: 'text/html'

  #php_admin_flag:
  #  log_errors: 'on'
```

## Example
```
- hosts: all
  roles:
   - role: php-fpm
```
