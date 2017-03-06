### cluster architecture considerations
* we are running 5 nodes
* let's do the best out of it (not recommended for prod!)
* let's use 2x master, 3x worker
* let's also deploy CM + Hue on first master
* let's furthermore use one worker for the third ZK and JN later

### node IPs and roles
* CM/Edge + Master1: 	ec2-54-93-77-231.eu-central-1.compute.amazonaws.com
* Master2:  		ec2-52-59-245-86.eu-central-1.compute.amazonaws.com	
* Worker1: 		ec2-54-93-33-31.eu-central-1.compute.amazonaws.com
* Worker2: 		ec2-54-93-43-116.eu-central-1.compute.amazonaws.com
* Worker3: 		ec2-52-59-195-41.eu-central-1.compute.amazonaws.com

### node/role assignment
* CM/Edge + Master1:    CM, Hue, NN, RM, ZK, JN, HMaster, HiveServer2
* Master2:              NN, RM, ZK, JN, HMaster, HiveServer2
* Worker1:              DN, NM, RS, HMaster 
* Worker2:              DN, NM, RS
* Worker3:              DN, NM, RS

### accessing CM
* http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180
