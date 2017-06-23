# multichain-python
Python package wrapper on top of [Multichain Blockchain](http://www.multichain.com/) with embedded multichain executables already bundled with the package.

# Prerequisite
1. install Anaconda 3+ suite (for environment variable CONDA_PREFIX = c:/anaconda/)

# install
1. Using Pip: 
`Pip install multichain`
 
2. Download/Clone to Desktop:
`python setup.py install`

# Use Example
```
>> import multichain
>> multichain.create("your_chain")
```
- Go to the created "%APPDATA%/MultiChain/your_chain/params.dat" for custom parameters. Once you start the blockchain this cannot be modified.
- Change username and password in the  "%APPDATA%/MultiChain/your_chain/multichain.conf"

After setting parameters then proceed with:

```
>> multichain.run(chainName)

>> rpcuser = "your_username"
>> rpcpasswd = "your_password"
>> rpchost = "127.0.0.1"
>> rpcport = "9568"
>> chainName = "your_chain"

>> api = multichain.api_call(rpcuser, rpcpasswd, rpchost, rpcport, chainName)

>> api.getinfo()
```

which outputs something as follows: 
```
{'balance': 0.0,
 'blocks': 59,
 'burnaddress': '1XXXXXXWxFXXXXXXCgXXXXXXYwXXXXXXX7DMtE',
 'chainname': 'chain0',
 'connections': 0,
 'description': 'MultiChain chain0',
 'difficulty': 6e-08,
 'errors': '',
 'incomingpaused': False,
 'keypoololdest': 1497889611,
 'keypoolsize': 2,
 'miningpaused': False,
 'nodeaddress': 'chain0@10.70.57.180:9569',
 'nodeversion': 10000201,
 'paytxfee': 0.0,
 'port': 9569,
 'protocol': 'multichain',
 'protocolversion': 10008,
 'proxy': '',
 'reindex': False,
 'relayfee': 0.0,
 'setupblocks': 60,
 'testnet': False,
 'timeoffset': 0,
 'version': '1.0 beta 1',
 'walletdbversion': 2,
 'walletversion': 60000}
```
All calls are methods to the api_call object: Ex: `api.multichain_api_call()`
