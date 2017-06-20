# multichain-python
Python wrapper on top of Multichain Blockchain with embedded multichain executables

# Prerequisite
1. install Anaconda 3+ suite (for environment variable CONDA_PREFIX)

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

All calls are methods to the api_call object: Ex: `api.multichain_api_call()`
