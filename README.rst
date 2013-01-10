Requests - SSLv3 Version
========================

What's this fork for?
---------------------

If you receive errors such as:

    SSLError: [Errno 1] _ssl.c:504: error:1407742E:SSL routines:SSL23_GET_SERVER_HELLO:tlsv1 alert protocol version

try using this fork. Everything is kept (relatively) to date with the [official
requests repo](https://github.com/kennethreitz/requests) except what is needed
to resolve this SSL issue.

Why not open an issue on requests?
----------------------------------

If you search the issues of official request repo, you'll see many issues
regarding the inability to easily select SSL versions. The issue seems to be
caused by OpenSSL on some Ubuntu machines, but requests has not adapted to this
issue.

Relevant issues:

* https://github.com/kennethreitz/requests/issues/606
* https://github.com/kennethreitz/requests/issues/625
* https://github.com/shazow/urllib3/pull/109

The resolution to most issues is "upgrade your Python" or "upgrade OpenSSL",
neither of which have worked for me. So this fork will contain my hack
found in [#799](https://github.com/kennethreitz/requests/pull/799) to make
requests work with sites that enforce SSLv3.
