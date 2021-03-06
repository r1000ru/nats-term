# Terminal client for NATS

Use for debug messages and requests in channels of NATS-server

### Install

Require installed NodeJS.

```
npm install -g nats-term
```

### Running

```bash
nats-term -t token -h 127.0.0.1 -p 4222
```
Parameter *-t* is optional, by default empty string
Parameters *-h* and *-p* is optional, by default: 127.0.0.1:4222

or

```bash
nats-term -u nats://token@hostname:port
```

### Use

If connect to NATS server is established, you can write commands in shell

### Commands

List of commands:
 - **HELP** - internal help
 - **SUB *channel*** - subscribe to channel. You will be receive all incoming message and requests (will require answer), while not unsubscribe channel.
 - **UNSUB *channel*** - unsubscribe from channel.
 - **LIST** - list active subscribes to channels.
 - **PUB *channel* *message*** - publish message to channel.
 - **REQ *channel* *message*** - send request to channel with message and wait response
 - **EXIT** - exit from client
