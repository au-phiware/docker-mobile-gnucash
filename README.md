# Usage

Create a `docker-compose.override.yml` and set the database passwords and expose
any ports and/or volumes you may require.

    version: '2'
    services:
      web:
        ports:
          - 80:80
          - 443:443
      database:
        environment:
          - 'MYSQL_PASSWORD=**secret**'
          - MYSQL_RANDOM_ROOT_PASSWORD=yes
        volumes:
          - /path/to/storage:/var/lib/mysql
        ports:
          - 3306:3306
      gnucash:
        volumes:
          - '/path/to/your/file.gnucash:/file.gnucash'

Then run `docker-compose up`.

You can then open your GnuCash file and use the *Save As...* function from the
*File* menu to import your data to the MySQL database running inside the
container.

It might be more convenient to import your data from your personally installed
GnuCash program. In this case, you only need to execute `docker-compose up web`
and the server address will be similar to `localhost` or `172.18.0.2`.
