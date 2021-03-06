===============================
Hyper: HTTP/2 Client for Python
===============================

.. image:: https://travis-ci.org/Lukasa/hyper.png?branch=master
    :target: https://travis-ci.org/Lukasa/hyper

HTTP is changing under our feet. HTTP/1.1, our old friend, is being
supplemented by the brand new HTTP/2 standard. HTTP/2 provides many benefits:
improved speed, lower bandwidth usage, better connection management, and more.

``hyper`` provides these benefits to your Python code. How? Like this::

    from hyper import HTTP20Connection

    conn = HTTP20Connection('twitter.com:443')
    conn.request('GET', '/')
    resp = conn.getresponse()

    print(resp.read())

Simple.

Caveat Emptor!
==============

Please be warned: ``hyper`` is in a very early alpha. You *will* encounter bugs
when using it. In addition, there are very many rough edges. With that said,
please try it out in your applications: I need your feedback to fix the bugs
and file down the rough edges.

Versions
========

``hyper`` provides support for draft 14 of the HTTP/2 draft specification and
draft 9 of the HPACK draft specification. As further drafts are released,
``hyper`` will be updated to support them.

Compatibility
=============

``hyper`` is intended to be a drop-in replacement for ``http.client``, with a
similar API. However, ``hyper`` intentionally does not name its classes the
same way ``http.client`` does. This is because most servers do not support
HTTP/2 at this time: I don't want you accidentally using ``hyper`` when you
wanted ``http.client``.

Contributing
============

``hyper`` welcomes contributions from anyone! Unlike many other projects we are
happy to accept cosmetic contributions and small contributions, in addition to
large feature requests and changes.

Before you contribute (either by opening an issue or filing a pull request),
please `read the contribution guidelines`_.

.. _read the contribution guidelines: http://hyper.readthedocs.org/en/development/contributing.html

License
=======

``hyper`` is made available under the MIT License. For more details, see the
``LICENSE`` file in the repository.

Authors
=======

``hyper`` is maintained by Cory Benfield, with contributions from others. For
more details about the contributors, please see ``CONTRIBUTORS.rst``.
