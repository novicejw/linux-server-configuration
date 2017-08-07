# Linux Server Configuration

## Network info:
**IP address**: `34.201.30.170`
**SSH port**: `2200`
**URL of catalog web app**: `http://34.201.30.170/`

## Software installed:

**General**: `finger`, `apache2`, `postgresql`, `mod-wsgi`, `pip`, `git`

**App-specific**: `flask`, `google-api-python-client` (oauth), `requests`, `sqlacademy`, `flask-sqlacademy`

## Configurations made:

### User Management
- Created a new user `grader` and gave `sudo` access to `grader`.
- Disabled `root` remote login.

### Security
- Updated all system applications.
- Changed SSH port from the default `22` to `2200`.
- Configured firewall to only allow for `SSH` (port 2200), `HTTP` (port 80), and `NTP` (port 123).
- Disabled password SSH authentication; only key-based SSH authentication allowed.

### Hosted Web Application
- Saved web app files in `/var/www/catalog`.
- Set up PostgreSQL database `catalog` for application, and populated with initial items.
- Configured web server to serve `catalog` application as WSGI app.
- Disabled directory listing in Apache.
- Disabled remote connections for PostgreSQL.
- Created database user `catalog` who is owner of `catalog` database.

## 3rd-party resources used:
- https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
