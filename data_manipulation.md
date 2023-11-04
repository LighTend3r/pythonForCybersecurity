
## Declaration

Bytes

```
var_bytes = b"my string in bytes"
```

Hexa
```
var_hexa = 0x546d
```


## String

```python
var_string = "ma string"
```

To bytes
```python
var_string.encode('utf-8') <=> m.encode()
var_string.encode('ascii')
#>>> b'ma string'
```

To hex
```python
var_string.encode('utf-8').hex()
#>>> 6d6120737472696e67
```
## Int

To bytes
```python
# pip install pycryptodome
from Crypto.Util.number import long_to_bytes
long_to_bytes(var_int)

# or

var_int=33
var_int.to_bytes(1, 'big')
#>>> b'!'

var_int = 1567
var_int.to_bytes(10, 'big')
#>>> b'\x00\x00\x00\x00\x00\x00\x00\x00\x06\x1f'
```

To String
```python
from Crypto.Util.number import long_to_bytes
long_to_bytes(var_int).decode()
```

To hexa
```python
hex(var_int)
```
## Bytes

To hexa
```python
var.hex()
```

To Int
```python
from Crypto.Util.number import bytes_to_long
bytes_to_long(var)
```

To String
```python
var.decode('utf-8')
```

## Hexa

To Int
```python
int(var_hexa_string,16)
```

To Bytes
```python
bytes.fromhex(var_hexa_string)
```

To String
```python
bytes.fromhex(var_hexa_string).decode()
```
