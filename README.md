# secureconn

This is a *basic* https-like implementation using [box](https://godoc.org/golang.org/x/crypto/nacl/box).

Basic meaning that we have a concept of a client and server that have a secure session. A handshake is performed in which they
trade public keys and begin a session. This utilizes public key encryption in that the sender uses the receiver's public key to encrypt the message. The receiver
decrpyts the message with their corresponding private key.

To use this:

```#!sh
$ git clone https://github.com/prologic/secureconn
$ go build
```

First, start the server:

```#!sh
$ ./secureconn -s [-p <port>]
```

Next, connect as a client:

```#!sh
$ ./secureconn [-p <port>]
```
