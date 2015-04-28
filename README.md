# a C10K server taking advantage of memcached's network library and websocket protocol
# 一个由memcached的网络库和websocket协议构成的长连接服务器

## Levin Add websoket support to memcached
* vllm@163.com

[USAGE]
    [.INSTALATION]
        [.1]install libevent
        [.2]./configure --with-libevent=/path/to/libevent/install/dir
        [.3]make
        [.4]make install
        [.5]/usr/local/bin/memcached -u root
    [.TEST WEBSOCK HANDSHAKE]
        [.6]open another terminal window
        [.7]connect server with websocket handshake header by client(written in PHP or anything you like)
        [.8]chek and enjoy it
        
[FUNTION]
    [.DONE]
        [..1]support websoket handshake
    [.TODO]
        [..2]support websoket full protocol
        [..3]code optimize 

## Dependencies

* libevent, http://www.monkey.org/~provos/libevent/ (libevent-dev)

## Environment

### Linux

If using Linux, you need a kernel with epoll.  Sure, libevent will
work with normal select, but it sucks.

epoll isn't in Linux 2.4, but there's a backport at:

    http://www.xmailserver.org/linux-patches/nio-improve.html

You want the epoll-lt patch (level-triggered).

## Website

* http://www.memcached.org

## Contributing

Want to contribute?  Up-to-date pointers should be at:

* http://contributing.appspot.com/memcached
