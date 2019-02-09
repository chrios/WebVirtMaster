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

# Planning

## Objectives

Allow multiple users to manage libvirt hypervisors from the web browser. virt-manager in the browser.

  - Display libvirt hypervisors
    - Domains
    - Networks
    - Storage
    - Host infomation
  - Manage hypervisors available in management system
    - Add libvirt connection
    - Remove libvirt connection
    - Change libvirt connection
  - Allow others to administor libvirt hypervisors
    - User accounts
    - Role based access control
  - Manage libvirt configuration
    - Add domain
    - Remove domain
    - Change domain configuration
    - Add network
    - Remove network
    - Change network configuration
    - Add storage pool
    - Remove storage pool
    - Change storage pool
      - Add disks
      - Remove disks
      - Extend disks
  - View VNC/Spice console of running domains

## URLs

Method | Location | Description
------ | -------- | -----------
GET | / | Login page
GET | /hypervisor | List of hypervisors
POST| /hypervisor/add | Add a new libvirt connection
DEL | /hypervisor/delete/libvirt-id | Delete a libvirt connection
PUT | /hypervisor/edit/libvirt-id | Edit a libvirt connection
GET | /hypervisor/info/libvirt-id | Hypervisor information
GET | /hypervisor/storage-pools/libvirt-id | Hypervisor storage pools
POST| /hypervisor/storage-pools/libvirt-id/create | Create storage pool on hypervisor
GET | /hypervisor/storage/libvirt-id/storage-id | Hypervisor storage pool information
PUT | /hypervisor/storage/libvirt-id/storage-id | Update hypervisor storage pool XML
GET | /hypervisor/domains/libvirt-id | Hypervisor domains 
POST| /hypervisor/domains/libvirt-id/create | Create domain
GET | /hypervisor/domain/libvirt-id/domain-id | Hypervisor domain information
PUT | /hypervisor/domain/libvirt-id/domain-id | Update domain XML
POST| /hypervisor/domain/libvirt-id/domain-id/delete | Delete domain
GET | /hypervisor/networks/libvirt-id | Hypervisor libvirt networks
POST| /hypervisor/networks/libvirt-id/add | Add libvirt network
GET | /hypervisor/network/libvirt-id/network-id | Hypervisor network information
PUT | /hypervisor/network/libvirt-id/network-id | Update network XML
GET | /hypervisor/console/libvirt-id/domain-id | Domain VNC console

## TODO

Add description of controller methods

Add description of model methods
