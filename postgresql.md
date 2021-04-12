## Installation
installation process below is for installation of specific version, in our case we need to install version `10` of `postgresql` as a requirement for `hivemind`
<br />

- Add PostgreSQL apt repository <br />
```# echo 'deb http://apt.postgresql.org/pub/repos/apt/ xenial-pgdg main' >> /etc/apt/sources.list.d/pgdg.list``` <br /> --make sure to change `xenial` to ubuntu version name you are using

- Import the repository signing key, and update the package lists <br />
```# wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -```

- Install Postgresql <br />
```# sudo apt-get update``` <br /> 
```# sudo apt-get install postgresql-10```
