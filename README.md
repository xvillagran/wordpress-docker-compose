# Wordpress Docker Compose
One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

 - Docker
 - Docker-compose

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
cd /path/to/your/work/dir
touch .env
nano .env
```
And then copy this and replace with your own values:
```
MYSQL_ROOT_PASSWORD=your_root_password
MYSQL_USER=your_wordpress_database_user
MYSQL_PASSWORD=your_wordpress_database_password
SITE_DOMAIN=www.example.com
ADMIN_EMAIL=someemail@mailnator.com
WORDPRESS_PATH=./wordpress
UID=1000
```

Get it up and running
```
docker-compose up
```
Go to http://127.0.01:8080 to complete the Wordpress installation

## Set up permissions to edit (optional)
Assuming that your host userd id is 1000
```
docker-compose exec wordpress bash
chown -R www-data:1000 wp-content/
chmod -R g+w wp-content/
exit
```

## Authors

* **Xuan Villagran**

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
## Acknowledgments

* Based on this great [guide](https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-with-docker-compose) by [Kathleen Juell](https://katjuell.site/)