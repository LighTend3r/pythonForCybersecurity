# PWN

The library `pwn` able to connect to a serveur

## Installation

```
apt-get update
apt-get install python3 python3-pip python3-dev git libssl-dev libffi-dev build-essential
python3 -m pip install --upgrade pip
python3 -m pip install --upgrade pwntools
```

## cheat sheet

### Connection

Connection to the server like `netcat`
```python
url = "http://url"
port = 1234
conn = remote(url, port)
```

Connection to a serveur with ssh
```
shell = ssh('user', 'host', password='password', port=22)
```

### Send data

#### For netcat
Send some data
```python
conn.send(var_bytes)
```

#### For SSH

```
shell['whoami']
#>>> b'bandit0'
```

### Reveive data

receive data
```python
conn.recvline()
#>>> b'Please specify the password.\r\n'
# or
conn.recvline(timeout=5)
```

receive until the texte `\n` is in response
```
conn.recvuntil(b'\n')
```

### Interation

Able to interact with shell/server
```python
conn.interactive()
```
