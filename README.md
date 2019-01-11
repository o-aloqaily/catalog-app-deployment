# Catalog App Project
This application provides a list of catalogs along with different items for each catalog that can be added by registered users. authentication is done via google sign in. It is deployed on an Ubuntu instance using Amazon lightsail.

## Project Information
- it is a required project for Udacity's FullStack Nanodegree Program.
- it was developed by Osama Aloqaily, https://github.com/o-aloqaily
- IP Address: 18.197.130.3
- You can also visit the website through 18.197.130.3.xip.io.

### Software
This project was developed using the following:
- flask framework.
- PostgreSQL database.
- SQLALchemy ORM.
- psycopg2 driver.
- Git.
- Python.
- pip package manager.
- Google OAuth related packages for authentication purposes.
- Other 3rd party packages needed for the project.


### Configuration
- This project was deployed on an Ubuntu (Linux) instance using Lightsail service from AWS.
- All dependencies were installed and all packages were updated.
- SSH connection port was changed from 22 to 2200. Lightsail firewall as well as ufw were configured accordingly.
- Uncomplicated firewall (UFW) were configured to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
- Some changes were made on sshd_config as follow:
    - SSH default port
    - PermitRootLogin was disabled
    - Password authentication was disabled allowing only keypair authentication.
- "grader" user has been created and added as a sudoer.
- SSH keypair was generated and public key was added to .ssh/authorized_keys to allow ssh connection with "grader" user.
- Timezone was changed to UTC.
- Apache, PostgreSQL, SQLALchemy and git packages were installed.
- "catalog" role was created for the database "catalog"
- This project was cloned into /var/www/html/catalog-app directory.
- Necessary configuration on the source code were made such as database connection parameters and a configuration module was generated in the same directory.
- `client_secret.json` file was updated accordingly utilizing xip.io service to allow for Google OAuth authentication.
- A .wsgi file was created for the project on /var/www/html/ directory.

