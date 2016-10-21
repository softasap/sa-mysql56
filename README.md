sa-mysql56
==========

[![Build Status](https://travis-ci.org/softasap/sa-mysql56.svg?branch=master)](https://travis-ci.org/softasap/sa-mysql56)

Drop-in sa-mysql compatible repository that installs mysql 5.6 on xenial systems. (By default set to 5.7 at a moment)

Example of usage (all parameters are optional)

Simple

  roles:
    - {
        role: "sa-mysql56"
      }


Advanced:


  roles:
    - {
        role: "sa-mysql56",
        mysql_root_user: root,
        mysql_root_password: devroot,
      - mysql_databases:
        - name: app_db
          encoding: utf8
          collation: utf8_general_ci
      - mysql_users:
        - name: app_user
          host: "%"
          password: dYud8LHBBptGN96LSn0e
          priv: "app_db.*:ALL"
      }




