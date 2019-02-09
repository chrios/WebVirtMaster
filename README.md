# WebVirtMaster
This is an experimental (for now) project to implement a web-based Hypervisor manager, written in PHP.

Currently the only non-commercial solutions are written in python, and are complicated to install and manage.

This project uses the following libraries:

  - https://libvirt.org/php/
  - https://www.codeigniter.com/
  - http://benedmunds.com/ion_auth/
  - https://getbootstrap.com/

## Installation

Ensure your web server has php-libvirt installed. You may need to build it as packages are not commonly available.

Modify application/views/test/header.php with your connection URI (if not connecting to libvirt on localhost).

Run the builtin php webserver in the git repo base directory (php -S localhost:80).

Have fun!

## Roadmap

  - Create REST structure
  - Implement user authentication
  - Hypervisor connection details including ssh keys in database
  - Multi hypervisor support
  - Impletement XML parsing and editing form for libvirt xml definitions
