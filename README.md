# pysui

Experimental (pre-alpha) python client side toolkit for Sui - WIP and expect significant refactoring

## Ready to run
Requires:
 * Linux or macos (x86_64 or M1)
 * python 3.10 or greater
 * pkg-config

## Run with devnet
By default, `pysui` will use the `client.yaml` configuration found in `.sui/sui_config/`. See [below](#run-local) for running
with different configuration (e.g. Local)

### Setup environment
`python3 -m venv pysuienv`

### Activate
`source pysuienv/bin/activate`

### Load packages
`pip list`

  * If you get a warning about upgrading pip... do so

`pip install -r requirements.txt` .

  * If you get an error with secp256k1 then:
    `pip install wheel` and try to install requirements again

### Run sample wallet app for help
`python -m samples.wallet`

#### Output
```bash
usage: wallet.py [-h] {active-address,addresses,gas,new-address,object,objects,package-object,package,rpcapi,transfer-sui,pay,merge-coin,split-coin,call,publish} ...

options:
  -h, --help            show this help message and exit

commands:
  {active-address,addresses,gas,new-address,object,objects,package-object,package,rpcapi,transfer-sui,pay,merge-coin,split-coin,call,publish}
    active-address      Shows active address
    addresses           Shows all addresses
    gas                 Shows gas objects
    new-address         Generate new address and keypair
    object              Show object by id
    objects             Show all objects
    package-object      Get raw package object with Move disassembly
    package             Get package definition
    rpcapi              Display Sui RPC API information
    transfer-sui        Transfer SUI gas to recipient
    pay                 Transfer SUI gas to recipient(s)
    merge-coin          Merge two coins together
    split-coin          Split coin into one or more coins
    call                Call a move contract function
    publish             Publish a SUI package
```

## Run Local
This is temporarily blocked due to v0.12.x issues running local SUI. Stay tuned....
### Known issues
https://github.com/MystenLabs/sui/issues/5461