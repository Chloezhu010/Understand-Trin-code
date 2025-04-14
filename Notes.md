# How to start Trin
- Link: https://github.com/ethereum/trin/tree/master/bin/trin/src
## main.rs
- Process
    - Setup async env
    - Init logging using ```init_tracing_logger```
    - Parse cmd line args into a ```TrinConfig``` structure
    - Launch by calling the ```run_trin``` async function,passing the config
    - Wait for a terminationa signal (Ctrl+C)
    - Stop RPC server upon shutdown
- Key functions
    - ```TrinConfig```: Handle config
    - ```run_trin```: Central coordinator to start Trin
## lib.rs
- ```run_trin```
    - Initization & Config
    - Core p2p setup
    - Storage factory
    - Subnetwork initialization
    - JSON-RPC server
    - Spawn background tasks