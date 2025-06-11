# Dual Mining
Dual Mining integrates third-party software and pools. Drpool does not track earnings from this part—please refer to your configured pool address for third-party software earnings.

Third parties control this fee rate—Drpool does not interfere.​​

Since third-party software is involved, Drpool cannot guarantee its stable operation. Miners should monitor it accordingly.

For any runtime issues, communicate in the community.

[Neptune + SRBMiner](#neptune--srbminer):NPT+XTM   
[Neptune + RigelMiner](#neptune--rigelminer):NTP+(ABEL/ALPH/ERG/ETC/.../QUAI)  
[Neptune + ONEZEROMiner](#neptune--onezerominer):NTP+(dynex/xelis/../zil)

## Neptune + SRBMiner

### ​Relevant materials
- **Pool**   https://tari.luckypool.io/
- **Prover** https://github.com/doktor83/SRBMiner-Multi

### Start

#### Setup on Ubuntu
- version >=1.0.6
   - ubuntu: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/tari/ubuntu-dr_neptune_prover-1.0.9.tar.gz
- Modify the `inner_guesser.sh` file
   ```sh
   #!/bin/bash

   # set your own drpool accountname
   accountname="accountname.miner001"
   
   pids=$(ps -ef | grep dr_neptune_prover | grep -v grep | awk '{print $2}')
   if [ -n "$pids" ]; then
       echo "$pids" | xargs kill
       sleep 5
   fi
   
   while true; do
       target=$(ps aux | grep dr_neptune_prover | grep -v grep)
       if [ -z "$target" ]; then
           ./dr_neptune_prover --pool stratum+tcp://neptune.drpool.io:30127 --worker $accountname --extra "srbminer_custom_bin;--algorithm;sha3x;--pool;tari.luckypool.io:6118;--wallet;<tariaddress>.<devicename>"
           sleep 5
       fi
       sleep 60
   done
   ```
   - `srbminer_custom_bin`: Software name (non-editable)​​
   - `tariaddress`: Replace with the miner's own Tari wallet address, [Statistics Overview](https://tari.luckypool.io/miner-stats#workers)  
   - `devicename`: Replace with the miner's own device name

#### Setup on HiveOS
- version >=1.0.6
   - hiveos: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/tari/nptprover-1.0.9.tar.gz
    ![alt text](image.png)
- Custom configuration->Extra config arguments:`--extra 'srbminer_custom_bin;--algorithm;sha3x;--pool;tari.luckypool.io:6118;--wallet;<tariaddress>.<devicename>'`
   - `srbminer_custom_bin`: Software name (non-editable)​​
   - `tariaddress`: Replace with the miner's own Tari wallet address, [Statistics Overview](https://tari.luckypool.io/miner-stats#workers)  
   - `devicename`: Replace with the miner's own device name
   - Other parameter descriptions refer to:​[Parameters](https://github.com/doktor83/SRBMiner-Multi/blob/master/Parameters), keys and values are linked by ";".

## Neptune + RigelMiner

### ​Relevant materials
GitHub: https://github.com/rigelminer/rigel

### Start

#### Setup on Ubuntu
- version >=1.0.8
   - ubuntu: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/rigel/ubuntu-dr_neptune_prover-1.0.9.tar.gz
- Modify the `inner_guesser.sh` file
   ```sh
   #!/bin/bash

   # set your own drpool accountname
   accountname="accountname.miner001"
   
   pids=$(ps -ef | grep dr_neptune_prover | grep -v grep | awk '{print $2}')
   if [ -n "$pids" ]; then
       echo "$pids" | xargs kill
       sleep 5
   fi
   
   while true; do
       target=$(ps aux | grep dr_neptune_prover | grep -v grep)
       if [ -z "$target" ]; then
           ./dr_neptune_prover --pool stratum+tcp://neptune.drpool.io:30127 --worker $accountname --extra "rigel;<>;<>;<>"
           sleep 5
       fi
       sleep 60
   done
   ```
   - `rigel`: Software name (non-editable)​​
   - [extra configuration](#extra-configuration)

#### Setup on HiveOS
- version >=1.0.8
   - hiveos: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/rigel/nptprover-1.0.9.tar.gz
- Custom configuration->Extra config arguments:`--extra 'rigel;<>;<>;<>'`
   - `rigel`: Software name (non-editable)​​
   - [extra configuration](#extra-configuration)

### extra configuration​

#### ETC

etc.sh
```sh
'./rigel -a etchash -o stratum+ssl://etc.2miners.com:11010 -u YOUR_ETC_WALLET -w my_rig --log-file logs/miner.log'
```

extra
```sh
--extra 'rigel;-a;etchash;-o;stratum+ssl://etc.2miners.com:11010;-u;YOUR_ETC_WALLET;-w;my_rig'
```

## Neptune + ONEZEROMINER

### ​Relevant materials
GitHub: https://github.com/OneZeroMiner/onezerominer (release 1.4.4)

### Start

#### Setup on Ubuntu
- version >=1.0.9
   - ubuntu: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/onezero/ubuntu-dr_neptune_prover-1.0.9.tar.gz
- Modify the `inner_guesser.sh` file
   ```sh
   #!/bin/bash

   # set your own drpool accountname
   accountname="accountname.miner001"
   
   pids=$(ps -ef | grep dr_neptune_prover | grep -v grep | awk '{print $2}')
   if [ -n "$pids" ]; then
       echo "$pids" | xargs kill
       sleep 5
   fi
   
   while true; do
       target=$(ps aux | grep dr_neptune_prover | grep -v grep)
       if [ -z "$target" ]; then
           ./dr_neptune_prover --pool stratum+tcp://neptune.drpool.io:30127 --worker $accountname --extra "onezerominer;<>;<>;<>"
           sleep 5
       fi
       sleep 60
   done
   ```
   - `rigel`: Software name (non-editable)​​
   - [extra configuration](#extra-configuration)

#### Setup on HiveOS
- version >=1.0.9
   - hiveos: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/onezero/nptprover-1.0.9.tar.gz
- Custom configuration->Extra config arguments:`--extra 'onezerominer;<>;<>;<>'`
   - `rigel`: Software name (non-editable)​​
   - [extra configuration](#extra-configuration)

### extra configuration​

#### XELIS

xelis.sh
```sh
./onezerominer -a xelis -w xel:zc0tqcru5sc8ry23e3ry7qk908g9aeqtvlmgahedkzgmcmrcqgyqqpu54e3 -o ssl://eu.xel.k1pool.com:9352 --worker rig_name
```

extra
```sh
--extra 'onezerominer;-a;xelis;-w;sxel:zc0tqcru5sc8ry23e3ry7qk908g9aeqtvlmgahedkzgmcmrcqgyqqpu54e3;-o;ssl://eu.xel.k1pool.com:9352;--worker;rig_name'
```
