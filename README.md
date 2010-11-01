libev Echo
====

A collection of simple examples for libev. Please fork and contribute.

Goal
----

A working implementation of `tcp`, `udp`, `unix stream socket`, and `unix dgram socket` echo servers from the same libev enabled binary.

Usage
====

unix-echo
---

Very simple working example. Not sure if it is 100% correct.

udp-echo
----

This example doesn't actually take advantage of any of the features of libev,
if I understand it correctly. I think it just wraps blocking code in libev.

  * `make`the `udp-echo` binary
  * start the `udp-echo` server in one terminal
  * test that you can see the open port `3333` in another
  * test that you see when `udp.js` connets by the message in the first terminal

Expected procedure and results:

    $ make udp-echo && ./udp-echo
    cc -Wall -Werror -lev -o udp-echo udp-echo.c
    udp_echo server started...


    $ netstat -lau | grep 3333
    udp        0      0 *:3333                  *:*

    $ node udp.js
    # this show up on the server window
    udp socket has become readable

Installing libev
====

    sudo apt-get install libev libev-dev

