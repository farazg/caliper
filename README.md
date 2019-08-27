## Changes

This is a fork of the Hyperledger Caliper project. Many setupts for different block sizes and network topologies have been added for Hyperledger Fabric networks. Also, Caliper produces three extra files along with the report it normally generates.

#### **These files are:**

* backlog_data.json - information about how the backlog of transactions develops over the course of the tests run by caliper. 
* docker_info.txt - A txt file containing information about the state of the docker containers after running caliper.
* results_all.json - A json file containing informaton about each transaction, with latency information for each stage, such as endorsement, ordering, etc. 

#### **Edited files:**
* packages\caliper-core\lib\caliper-flow.js
* packages\caliper-core\lib\transaction-status.js
* packages\caliper-core\lib\client\client-orchestrator.js
* packages\caliper-fabric-ccp\lib\fabric.js
* packages\caliper-core\lib\gui\src\demo.js

#### **Added files:**
* packages\caliper-application\benchmark\smallbank\config_linear_100_1200.yaml
* packages\caliper-application\benchmark\smallbank\config_linear_400_800.yaml
* packages\caliper-application\benchmark\smallbank\config_linear_900_1100.yaml
* packages\caliper-application\benchmark\smallbank\config_linear_1000_1200.yaml
* packages\caliper-application\benchmark\smallbank\config_long_100000.yaml
* packages\caliper-application\benchmark\simple\config_linear_100_1200.yaml
* packages\caliper-application\benchmark\simple\config_linear_400_800.yaml
* packages\caliper-application\benchmark\simple\config_linear_900_1100.yaml
* packages\caliper-application\benchmark\simple\config_linear_1000_1200.yaml
* packages\caliper-application\benchmark\simple\config_linear_my.yaml

* packages\caliper-application\network\fabric-v1.1\3org3peergoleveldb
* packages\caliper-application\network\fabric-v1.1\3org3peergoleveldb\docker-compose.yaml
* packages\caliper-application\network\fabric-v1.1\3org3peergoleveldb\fabric-ccp-node.yaml
* packages\caliper-application\network\fabric-v1.2\3org3peergoleveldb
* packages\caliper-application\network\fabric-v1.2\3org3peergoleveldb\docker-compose.yaml
* packages\caliper-application\network\fabric-v1.2\3org3peergoleveldb\fabric-ccp-node.yaml
* packages\caliper-application\network\fabric-v1.3\3org3peergoleveldb
* packages\caliper-application\network\fabric-v1.3\3org3peergoleveldb\docker-compose.yaml
* packages\caliper-application\network\fabric-v1.3\3org3peergoleveldb\fabric-ccp-node.yaml
* packages\caliper-application\network\fabric-v1.4\3org3peergoleveldb
* packages\caliper-application\network\fabric-v1.4\3org3peergoleveldb\docker-compose.yaml
* packages\caliper-application\network\fabric-v1.4\3org3peergoleveldb\fabric-ccp-node.yaml


### **Created and added all folders and files in these folders (configs, setups, certificates, network-topologies, genesis-blocks, etc..):**
* packages\caliper-application\network\fabric-v1.1\block150
* packages\caliper-application\network\fabric-v1.1\block150_org
* packages\caliper-application\network\fabric-v1.1\block150manypeers
* packages\caliper-application\network\fabric-v1.1\block200
* packages\caliper-application\network\fabric-v1.1\block250
* packages\caliper-application\network\fabric-v1.1\block300
* packages\caliper-application\network\fabric-v1.1\block350
* packages\caliper-application\network\fabric-v1.1\block400
* packages\caliper-application\network\fabric-v1.1\block450
* packages\caliper-application\network\fabric-v1.1\block500
* packages\caliper-application\network\fabric-v1.2\block150
* packages\caliper-application\network\fabric-v1.2\block150_org
* packages\caliper-application\network\fabric-v1.2\block150manypeers
* packages\caliper-application\network\fabric-v1.2\block200
* packages\caliper-application\network\fabric-v1.2\block250
* packages\caliper-application\network\fabric-v1.2\block300
* packages\caliper-application\network\fabric-v1.2\block350
* packages\caliper-application\network\fabric-v1.2\block400
* packages\caliper-application\network\fabric-v1.2\block450
* packages\caliper-application\network\fabric-v1.2\block500
* packages\caliper-application\network\fabric-v1.3\block150
* packages\caliper-application\network\fabric-v1.3\block150_org
* packages\caliper-application\network\fabric-v1.3\block150manypeers
* packages\caliper-application\network\fabric-v1.3\block200
* packages\caliper-application\network\fabric-v1.3\block250
* packages\caliper-application\network\fabric-v1.3\block300
* packages\caliper-application\network\fabric-v1.3\block350
* packages\caliper-application\network\fabric-v1.3\block400
* packages\caliper-application\network\fabric-v1.3\block450
* packages\caliper-application\network\fabric-v1.3\block500
* packages\caliper-application\network\fabric-v1.4\block150
* packages\caliper-application\network\fabric-v1.4\block150_org
* packages\caliper-application\network\fabric-v1.4\block150manypeers
* packages\caliper-application\network\fabric-v1.41\block200
* packages\caliper-application\network\fabric-v1.4\block250
* packages\caliper-application\network\fabric-v1.4\block300
* packages\caliper-application\network\fabric-v1.4\block350
* packages\caliper-application\network\fabric-v1.4\block400
* packages\caliper-application\network\fabric-v1.4\block450
* packages\caliper-application\network\fabric-v1.4\block500


## Hyperledger Caliper

Welcome to the Hyperledger Caliper project. Caliper is a blockchain performance benchmark framework, which allows users to test different blockchain solutions with predefined use cases, and get a set of performance test results.

Currently supported blockchain solutions:
* [fabric v1.0+](https://github.com/hyperledger/fabric), the lastest version that has been verified is v1.1.0
* [sawtooth 1.0+](https://github.com/hyperledger/sawtooth-core)
* [Iroha 1.0 beta-3](https://github.com/hyperledger/iroha)
* [Burrow 1.0](https://github.com/hyperledger/burrow)

[Hyperledger Composer](https://github.com/hyperledger/composer) is also supported.

Currently supported performance indicators:
* Success rate
* Transaction/Read throughput
* Transaction/Read latency(minimum, maximum, average, percentile)
* Resource consumption (CPU, Memory, Network IO,...)

See [to add the link to PSWG] to find out the definitions and corresponding measurement methods.  

For more information please consult the [documentation site](https://hyperledger.github.io/caliper/)

## How to contribute

We welcome contributions to the Caliper code base. Please see [Contributing](/CONTRIBUTING.md) for more information.

## License
The Caliper codebase is release under the [Apache 2.0 license](./LICENSE). Any documentation developed by the Caliper Project is licensed under the Creative Commons Attribution 4.0 International License. You may obtain a copy of the license, titled CC-BY-4.0, at http://creativecommons.org/licenses/by/4.0/.
