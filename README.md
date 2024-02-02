Welcome to Kagopow 
===========================

# Wallets
- [Download Kagopow Core wallet for Windows](#)
- [Download Kagopow Core wallet for Macos](#)
- [Download Kagopow Core wallet for Ubuntu](#)

# Coin specifications:
&nbsp; | &nbsp;
------ | ------
**Coin name:** | KAGOPOW (KAGO)
**Initial block reward:** | 100 KAGO
**Initial block reward (POS):** | 20 KAGO
**Algorithm:** | Scrypt (Proof of Work and Proof of Stake)
**Premine:** | 100000 KAGO
**Coinbase maturity** | 20 (+ 1 default confirmation) blocks
**Target spacing** | 2 Minutes
**Target timespan** | 10 Minutes
**Transaction confirmations** | 6 (+ 1 default confirmation) blocks


kagopow.conf configuration:
----------------

```
listen=1
server=1
rpcport=9492
port=9493
rpcuser=(your_rpc_username)
rpcpassword=(your_rpc_password)
rpcconnect=127.0.0.1
rpcallowip=127.0.0.1

# NODE CONFIGURATION
addnode=159.223.80.240
```

Build
-------
```bash
./autogen.sh && \
./contrib/install_db4.sh `pwd` && \
export BDB_PREFIX=$PWD/db4 && \
./configure BDB_LIBS="-L${BDB_PREFIX}/lib -ldb_cxx-4.8" BDB_CFLAGS="-I${BDB_PREFIX}/include" && \
make -j$(nproc) && \
make check -j$(nproc)
```


License
-------

Kagopow Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.