# Basic Deploy

Simple web page deployment project containing:

- Vagrant
- VirtualBox
- Ansible
- Nginx
- Docker

## Frontend

- HTML

## Backend

- Ruby

# Getting Started

## Setup Requirements

Vagrant and Ansible installed.

## Usage

Run `vagrant up` on your terminal and access _localhost_ on your browser.

# How It Works

Running "vagrant up", will trigger the provisioning (Ansible) in the guest machine (Vagrant). This provisioning is configured in _./provisioning/site.yml_ and is responsible for installing required packages and Docker before starting the Nginx container.
