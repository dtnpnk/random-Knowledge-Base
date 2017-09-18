# Tunneling / Port Forwarding \(EN\) {#tunnelingport_forwarding_en}

Bearbeiten

## Introduction {#introduction}

Bearbeiten

### 1. local: {#local}

* `-L`
  Specifies that the given port on the local \(client\) host is to be forwarded to the given host and port on the remote side.
* `ssh -L sourcePort:forwardToHost:onPort`connectToHost means: connect with ssh to`connectToHost`, and forward all connection attempts to the **local **`sourcePort`to port`onPort`on the machine called`forwardToHost`, which can be reached from the`connectToHost`machine.

```
 your host              remotehost
╔══════════╗           ╔══════════╗
║          ║           ║localhost ║
║          ║           ║          ║
║         L:123-------R:456       ║
╚══════════╝           ╚══════════╝
```

```
 your host             remotehost             faraway host
╔══════════╗          ╔══════════╗            ╔══════════╗
║          ║          ║          ║            ║          ║
║          ║          ║          ║            ║          ║
║         L:123------------------------------R:456       ║
╚══════════╝          ╚══════════╝            ╚══════════╝
```


