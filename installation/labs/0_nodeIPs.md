### cluster architecture considerations
*we are running 5 nodes
*let's do the best out of it (not recommended for prod!)
*let's use 2x master, 3x worker
*let's also deploy CM + Hue on first master
*let's furthermore use one worker for the third ZK and JN later

### node IPs and roles
* CM/Edge + Master1: 	54.93.98.230
* Master2:  		54.93.143.230
* Worker1: 		54.93.205.173
* Worker2: 		54.93.114.58
* Worker3: 		54.93.202.201

### node/role assignment
* CM/Edge + Master1:    CM, Hue, NN, RM, ZK, JN, HMaster, HiveServer2
* Master2:              NN, RM, ZK, JN, HMaster, HiveServer2
* Worker1:              DN, NM, RS, HMaster 
* Worker2:              DN, NM, RS
* Worker3:              DN, NM, RS
