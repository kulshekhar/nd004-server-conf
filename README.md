# nd004 Server Conf

### Project details:
- IP Address: 45.55.163.30
- SSH Port: 2200
- URL to hosted web app: http://45.55.163.30
- Software installed:
  - Update sources and upgrade all packages
  - Apache
  - Postgres
  - Python Pip (and other dependencies like `build-essential`, etc)
  - Python packages using pip (flask, etc)
- Configuration changes
  - Disable root login
  - Create user `grader`
  - Grant sudo acccess to `grader`
  - Prevent password login
  - Allow `grader` to login using key
  - Set SSH to use a non default port
  - Set the firewall to close all incoming connections except on port 80, 2200 and 123
  - Configure the web app to run as a WSGI app using Apache

### Note about application

The installed application doesn't have a valid 'secret' file that would be required to use Google authentication for logging in.
Consequently, while the app will work, some of its functionality (logging in, creating new items, editing and deleting those items) will not be available.
