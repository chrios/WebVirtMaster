# WebVirtMaster
This is an experimental (for now) project to implement a web-based Hypervisor manager, written in PHP.

This project uses the following libraries:

  - https://libvirt.org/php/
  - https://www.codeigniter.com/
  - http://benedmunds.com/ion_auth/

To install:

Ensure your web server has php-libvirt installed. You may need to build it as packages are not commonly available.

Modify application/views/test/header.php with your connection URI (if not connecting to libvirt on localhost).

Run the builtin php webserver in the git repo base directory (php -S localhost:80).

Have fun!
