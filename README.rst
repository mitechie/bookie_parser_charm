Overview
========

Install an instance of the readable parsing application. See http://r.bmark.us
for the primary instance.

Provides a bookmarklet for quickly taking a web page and turning it into a
readable view.

Installation
============

You will need to have `Juju`_ installed and an environment `bootstrapped`_.
To deploy `bookie_parser` you will also need a Redis instance.


::

    juju deploy redis-master --constraints instance-type=t1.micro
    juju deploy cs:~juju-jitsu/precise/bookie_parser --constraints instance-type=t1.micro
    juju add-relation bookie_parser redis-master
    juju expose bookie_parser



.. _Juju: http://juju.ubuntu.com
.. _bootstrapped: https://juju.ubuntu.com/docs/getting-started.html
