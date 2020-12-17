# Basic Deploy

Simple web page deployment project

## Structure & Components

- Vagrant
- VirtualBox
- Ansible
- Docker
- Nginx

### Frontend

- HTML
- CSS

## Getting Started

### Setup Requirements

Vagrant and Ansible installed.

### Usage

Run `vagrant up` on your terminal and access _localhost:1234_ on your browser.

## How It Works

Running "vagrant up", will bring an Ubuntu machine up and trigger the provisioning (Ansible) in the guest machine (Vagrant). This provisioning is configured in _./provisioning/site.yml_, divided by roles, and it's responsible for installing required packages and Docker before starting the Nginx container.
