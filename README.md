# UnicodeDecodeError
>>> import gmpy2
>>> from Crypto.Util.number import long_to_bytes
>>> gmpy2.get_context.precision = 2048
Traceback (most recent call last):
  File "<pyshell#61>", line 1, in <module>
    gmpy2.get_context.precision = 2048
AttributeError: 'builtin_function_or_method' object has no attribute 'precision'
>>> gmpy2.get_context().precision=2048
>>> pt = gmpy.root(ct,e)
Traceback (most recent call last):
  File "<pyshell#63>", line 1, in <module>
    pt = gmpy.root(ct,e)
NameError: name 'gmpy' is not defined
>>> pt = gmpy2.root(ct,e)
>>> print(long-to-bytes(pt).decode())
Traceback (most recent call last):
  File "<pyshell#65>", line 1, in <module>
    print(long-to-bytes(pt).decode())
NameError: name 'long' is not defined
>>> print(long_to_bytes(pt).decode())
Traceback (most recent call last):
  File "<pyshell#66>", line 1, in <module>
    print(long_to_bytes(pt).decode())
UnicodeDecodeError: 'utf-8' codec can't decode byte 0x83 in position 3: invalid start byte
