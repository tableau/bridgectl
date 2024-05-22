

## Driver Caddy 
Driver Caddy makes it easy to install and test database drivers by defining a standard YAML Driver installation definition file that can be used to generate specific scripts for various target operating systems and container or virtual machine runtimes. 


Here is an example YAML file:

```
---
- driver: postgresql
  os: rhel8, rhel9,amazonlinux2023
  download_url: https://jdbc.postgresql.org/download/postgresql-42.3.4.jar
  type: jar
```