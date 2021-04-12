## Installation
Installation process below is for installation of specific version, in our case we need to install version `10` of `postgresql` as a requirement for `hivemind`
<br />

- Add PostgreSQL apt repository <br />
```# echo 'deb http://apt.postgresql.org/pub/repos/apt/ xenial-pgdg main' >> /etc/apt/sources.list.d/pgdg.list``` <br /> --make sure to change `xenial` to ubuntu version name you are using

- Import the repository signing key, and update the package lists <br />
```# wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -```

- Install Postgresql <br />
```# sudo apt-get update``` <br /> 
```# sudo apt-get install postgresql-10```

## Remote connection
In order to connect to postgresql database remotely we need to tweak postgres configuration, you can use `SHOW config_file` and `SHOW hba_file` inside `psql` to locate the configuration files

- Change Listen Address in postgresql.conf <br />
```listen_addresses = '*'```

- Configure pg_hba.conf <br />
```host    all      all              0.0.0.0/0                    md5 ``` <br />
```host    all      all              ::/0                         md5```

- Restart services <br />
```systemctl restart postgresql.service```
