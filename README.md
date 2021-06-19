# solo-mine

RPC Tools
---------------------

### [RPCUser](/share/rpcuser) ###

Create an RPC user login credential.

Usage:

    ./rpcuser.py <username>
 
 that is:  ./rpcuser.py username
    
 ### Result from above
 
 ```
 String to be appended to xazab.conf:
rpcauth=username:d02ef158d8c8a88c899a8888e8888a21i99a987a88a77a88a88a88a88aa7ae
Your password:  hIuIAMwb3OJxMON-dJorUi3UYD72AduE21Uy2=
```
  
### Configure Xazab.conf

```
server=1
listen=1
rpcallowip=127.0.0.1
rpcallowip=198.44.2.30/24
algo=lyra2
gen=0
rpcauth=username:d02ef158d8c8a88c899a8888e8888a21i99a987a88a77a88a88a88a88aa7ae
```
**More algorithm to use include: algo=sha256d, algo=scrypt, algo=yespower, algo=x11**

Save the above and run the xazab-qt or xazabd wallet

Miner:

You can get your cpuminer and run it like this

```shell
./cpuminer-avx2.exe --algo=lyra2z330 -o http://127.0.0.1:31313 -u username -p hIuIAMwb3OJxMON-dJorUi3UYD72AduE21Uy2= --no-stratum --no-getwork --no-extranonce --coinbase-addr=XsYVT5uPiv1CGHs8tyWkqeTS875xDUTYMp

```
