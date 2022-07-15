# Configure packages

Follows are the list of references to follow and steps to get a package working as intended:

> Some configs have already been included in my [**_dotfiles_**](https://github.com/vuong-cuong-phoenix/dotfiles)

## `asdf-vm`

1. [Getting started](https://asdf-vm.com/guide/getting-started.html)
2. Install [`ruby`](https://github.com/asdf-vm/asdf-ruby) and [`nodejs`](https://github.com/asdf-vm/asdf-nodejs) plugins.

## `rustup`

1. Install both `nightly` and `stable` toolchains:

    ```sh
    rustup toolchain install nightly
    rustup toolchain install stable
    ```

2. Choose `nightly` as the default toolchain:

    ```sh
    rustup default nightly
    ```

## `postgres`

1. [Installation](https://wiki.archlinux.org/title/PostgreSQL#Installation)
2. [Initial configuration](https://wiki.archlinux.org/title/PostgreSQL#Initial_configuration)
3. [Create database & user with the same name as the current user](https://wiki.archlinux.org/title/PostgreSQL#Create_your_first_database/user)
4. [Setup SSL/TLS](https://www.postgresql.org/docs/current/ssl-tcp.html)

    - Create certificate(s) and key(s) using `mkcert`, remember to run as a client (normal) user:

      ```sh
      mkcert -install # Run this if not ran before.
      mkcert -cert-file server.crt -key-file server.key localhost
      ```

    - Move server certificate and key using `mkcert` and change owner of those files, run as root:

      ```sh
      mv server.crt /var/lib/postgres/data
      mv server.key /var/lib/postgres/data
      chown postgres:postgres /var/lib/postgres/data/server.crt /var/lib/postgres/data/server.key
      ```

## `mariadb`

1. [Installation](https://wiki.archlinux.org/title/MariaDB#Installation).
2. [Add user with the same name as the current user](https://wiki.archlinux.org/title/MariaDB#Add_user).
3. [Enable auto-completion](https://wiki.archlinux.org/title/MariaDB#Enable_auto-completion).
4. [Populate timezone tables](https://wiki.archlinux.org/title/MariaDB#Time_zone_tables).

## `docker`

1. [Installation](https://wiki.archlinux.org/title/Docker#Installation).
    _Note:_ If you want to be able to run the `docker` CLI command as a non-root user, add your user to the `docker` user group, re-login, and restart `docker.service`.

## `samba`

1. [Installation](https://wiki.archlinux.org/title/Samba#Installation)
2. [Configure firewall using `firewalld`](https://wiki.archlinux.org/title/Samba#firewalld_service)
3. [Add a user](https://wiki.archlinux.org/title/Samba#Adding_a_user)
4. [Enable Usershares](https://wiki.archlinux.org/title/Samba#Enable_Usershares)

## `syncthing`

1. [Installation](https://wiki.archlinux.org/title/Syncthing#Installation)
2. [Autostart Syncthing using user service](https://wiki.archlinux.org/title/Syncthing#User_service)
