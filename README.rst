===============================
Hyper: HTTP/2 Client for Python
===============================

This package is only maintained for compatibility with Django Push Notifications. It is not to be used in new projects.

``hyper`` is a Python package that provides an HTTP/2 client implementation.

An example of usage is::

    from hyper import HTTPConnection

    conn = HTTPConnection('nghttp2.org:443')
    conn.request('GET', '/httpbin/')
    resp = conn.get_response()

    print(resp.read())

Simple.

Caveat Emptor!
==============

Please be warned: ``hyper`` is in a very early alpha. You *will* encounter bugs
when using it. In addition, there are very many rough edges.

Versions
========

``hyper`` supports the final draft of the HTTP/2 specification: additionally,
it provides support for drafts 14, 15, and 16 of the HTTP/2 specification. It
also supports the final draft of the HPACK specification.

Compatibility
=============

``hyper`` is intended to be a drop-in replacement for ``http.client``, with a
similar API. However, ``hyper`` intentionally does not name its classes the
same way ``http.client`` does. This is because most servers do not support
HTTP/2 at this time: I don't want you accidentally using ``hyper`` when you
wanted ``http.client``.

Documentation
=============

Looking to learn more? Documentation for ``hyper`` can be found on `Read the Docs`_.

.. _Read the Docs: http://hyper.readthedocs.io/en/latest/

License
=======

``hyper`` is made available under the MIT License. For more details, see the
``LICENSE`` file in the repository.

Authors
=======

``hyper`` was originally maintained by Cory Benfield, with contributions from others. This fork is only maintained for
Python compatibility.
