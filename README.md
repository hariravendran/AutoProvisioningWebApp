# Automated Provisioning for VentureHub Project

## Overview

This repository contains scripts and configurations to automate the setup of a multi-tier web application stack for the **VentureHub Project**. Designed for both Windows and macOS (Intel), this project leverages Vagrant and VirtualBox to create a local development environment that is repeatable and easy to manage.

## Prerequisites

Before you begin, ensure you have the following tools installed:

- **Oracle VM VirtualBox**: A powerful x86 and AMD64 virtualization product for enterprise as well as home use.
- **Vagrant**: A tool for building and managing virtualized development environments.
- **Git Bash**: A command line interface for Windows that provides a bash emulation.
- (Optional) An IDE or text editor (e.g., Visual Studio Code, Sublime Text, Notepad++).

## Repository Structure

```
/Automated_provisioning
    ├── vagrant
        ├── Vagrantfile
        ├── mysql.sh
        ├── memcache.sh
        ├── rabbitmq.sh
        ├── tomcat.sh
        └── nginx.sh
```

- **Vagrantfile**: Configuration file for Vagrant that defines the virtual machines and their settings.
- **mysql.sh**: Shell script for provisioning the MariaDB service.
- **memcache.sh**: Shell script for provisioning the Memcached service.
- **rabbitmq.sh**: Shell script for provisioning the RabbitMQ service.
- **tomcat.sh**: Shell script for provisioning the Tomcat server.
- **nginx.sh**: Shell script for provisioning the Nginx web server.

## Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/hariravendran/AutoProvisioningWebApp/
   (Extract Automated_provisioning_WinMacIntel.zip)
   cd Automated_provisioning_WinMacIntel
   ```

2. **Start the Vagrant Environment**:
   - Open Git Bash and run the following command:
     ```bash
     vagrant up
     ```
   - This command will start the provisioning process for all defined VMs.

3. **Access the Application**:
   - Once provisioning is complete, you can access the web application using the static IP or hostname defined in the Vagrantfile. Open your browser and navigate to:
     ```
     http://web01
     ```

4. **Logging In**:
   - Use the credentials:
     - **Username**: `admin_vp`
     - **Password**: `admin_vp`

## Managing the Environment

- **To halt all VMs**:
  ```bash
  vagrant halt
  ```

- **To check the status of VMs**:
  ```bash
  vagrant status
  ```

- **To bring the VMs back up without provisioning**:
  ```bash
  vagrant up
  ```

## Conclusion

This automated setup streamlines the process of creating a multi-tier web application stack for the **VentureHub Project** on your local machine. By using Vagrant and the provided provisioning scripts, you can easily manage and repeat the setup for development and testing purposes.
Feel free to explore the scripts and modify them according to your project needs.

## License

This project is licensed under the MIT License.
