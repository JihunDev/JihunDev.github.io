---
title: Postgresql Error pg_config executable not found.
author: Jihun Kim
date: 2021-11-28 00:00:00 +0000
categories: [Postgresql]
tags: [Postgresql]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# 오류 메세지
```bash
Collecting psycopg2
  Using cached https://files.pythonhosted.org/packages/c7/ca/75236b17f1b951950ffc55d657c5aa408d3d0327a1b6c4c0f7cb16ef7e7b/psycopg2-2.8.tar.gz
    Complete output from command python setup.py egg_info:
    running egg_info
    creating pip-egg-info/psycopg2.egg-info
    writing pip-egg-info/psycopg2.egg-info/PKG-INFO
    writing dependency_links to pip-egg-info/psycopg2.egg-info/dependency_links.txt
    writing top-level names to pip-egg-info/psycopg2.egg-info/top_level.txt
    writing manifest file 'pip-egg-info/psycopg2.egg-info/SOURCES.txt'

    Error: pg_config executable not found.

    pg_config is required to build psycopg2 from source.  Please add the directory
    containing pg_config to the $PATH or specify the full executable path with the
    option:

        python setup.py build_ext --pg-config /path/to/pg_config build ...

    or with the pg_config option in 'setup.cfg'.

    If you prefer to avoid building psycopg2 from source, please install the PyPI
    'psycopg2-binary' package instead.

    For further information please check the 'doc/src/install.rst' file (also at
    <http://initd.org/psycopg/docs/install.html>).

    ----------------------------------------
Command "python setup.py egg_info" failed with error code 1 in /private/var/folders/7m/gd92t9wx0nl_t8yw70ymhl0c0000gn/T/pip-install-t4927zna/psycopg2/
```

- pip로 psycopg2-binay 설치시 Path 관련 오류

# Solution

- psycopg2-binary 설치시 시스템 postgresql에 종속성을 갖는다

```bash
$ brew install postgresql
```