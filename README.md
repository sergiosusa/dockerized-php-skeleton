# 🐋Dockerized PHP Skeleton🐋

Complete Dockerized developer stack for PHP developers.

Includes:

- Nginx.
- Mysql.
- PHP (extensions, composer, so on.).

Also, includes a bash tool to initialize the docker containers and Symfony 7 project easily.

# 🖥️Installation🖱️

## Linux/Mac

- Clone the project.
- Run ``./tools init-containers`` to build and start all the containers.

if you need an empty Symfony 7 Project:

- Run ``./tools init-symfony-project symfony/skeleton:"7.1.*"`` to initialize the Symfony 7 project.
- Add ``0.0.0.0 project.local`` to ``/etc/hosts``.
- Go to the browser and enter to: http://project.local/.

That's it!

## Windows

- You have to [install WSL](https://learn.microsoft.com/en-us/windows/wsl/install).
- Run ``./tools init-containers`` to build and start all the containers.

> **Note:** If you get some error executing the bash script could be that the format of the file is not Unix (LF), to
> convert it you need to use dos2unix.
>
> ``sudo apt install dos2unix``
> 
> ``dos2unix tools``

if you need an empty Symfony 7 Project:

- Run ``./tools init-symfony-project symfony/skeleton:"7.1.*"`` to initialize the Symfony 7 project.
- Add ``127.0.0.1 project.local`` to ``/etc/hosts``.
- Go to the browser and enter to: http://project.local/.

That's it!

### Tools script

Run ``./tools help`` to see all available options.

### Project based on

- [Docker with shell script or Makefile](https://ypereirareis.github.io/blog/2015/05/04/docker-with-shell-script-or-makefile/)
- [Awk Find And Replace Fields Values](https://www.cyberciti.biz/faq/awk-find-and-replace-fields-values/)

**Special thanks to:**

[Berny Cantos](https://github.com/xphere) Who showed me how to fix the user's permission problems.