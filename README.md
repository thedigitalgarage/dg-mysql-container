MySQL Docker images
===================

This repository contains Dockerfiles for MySQL images for the Digital Garage.

For more information about using these images with OpenShift, please see the
official [Digital Garage Documentation](https://docs.thedigitalgarage.io/using_images/db_images/mysql.html)


Versions
---------------
MySQL versions currently provided are:
* mysql-5.5
* mysql-5.6


Installation
----------------------

 This image is available on DockerHub. To download it run:

    ```
    $ docker pull thedigitalgarage/mysql-55-centos7
    ```

 or

    ```
    $ docker pull thedigitalgarage/mysql-56-centos7
    ```

 To build a MySQL image from scratch run:

    ```
    $ git clone https://github.com/thedigitalgarage/mysql.git
    $ cd mysql
    $ make build VERSION=5.5
    ```

For using other versions of mysql, just replace the `5.5` value by particular version
in the commands above.

**Notice: By omitting the `VERSION` parameter, the build/test action will be performed
on all provided versions of MySQL, which must be specified in  `VERSIONS` variable.
This variable must be set to a list with possible versions (subdirectories).**


Usage
---------------------------------

For information about usage of Dockerfile for MySQL 5.6,
see [usage documentation](5.6/README.md).

For information about usage of Dockerfile for MySQL 5.5,
see [usage documentation](5.5/README.md).


Test
---------------------------------

This repository also provides a test framework, which checks basic functionality
of the MySQL image.

    ```
    $ cd mysql
    $ make test VERSION=5.5
    ```

For using other versions of mysql, just replace the `5.5` value by particular version
in the commands above.

**Notice: By omitting the `VERSION` parameter, the build/test action will be performed
on all provided versions of MySQL, which must be specified in  `VERSIONS` variable.
This variable must be set to a list with possible versions (subdirectories).**
