#### An Ambari Service for Hue
Ambari service for easily installing and managing Hue 3.11.0 on HDP 2.x cluster.  This repository is updated with only the minimal changes required for Kyle's original repo to install.  If you need to understand the differences please diff each repo.

#### Authors
  - [Kyle Joe](https://github.com/EsharEditor)
  - [Steven Matison](https://github.com/steven-matison)

#### Notes
- A big thank you to Kyle for creating the original HDP 2.x github repo. Have a look here:  https://github.com/EsharEditor/ambari-hue-service

- See https://gethue.com for more information, versions, and official documentation.
- Working on Hue 4.x with HDP 3.x [HERE](https://github.com/steven-matison/HDP3-Hue-Service)
- Working on Hue Management Pack for Ambari [HERE](https://github.com/steven-matison/dfhz_hue_mpack)
- Working with Hue 4.x with HDP 2.x [HERE](https://github.com/steven-matison/HDP2-Hue4-Service)

#### Version
- Hue 3.11.0
- HDP 2.x

#### Setup
- Install required services: HDFS,Yarn,Hive,Hbase,Spark,Zookeeper,Sqoop,Oozie,Pig,Tez,etc
- Install epel repository OR Make sure all gethue.com dependencies are able to be installed on hue node
- Deliver Service Fileset to Ambari   
``` 
sudo git clone https://github.com/steven-matison/HDP2-Hue-Service.git /var/lib/ambari-server/resources/stacks/HDP/[version]/services/HUE
```
  **** be sure to get your correct [version] for command above
- Restart Ambari
```
service ambari-server restart
```
- In Ambari click on 'Add Service' and install HUE

#### Known Issues
- Very long install time due to compile time for Hue's make install command

#### Coming Soon
- HDP 2.x Management Pack [dfhz_hue_mpack](https://github.com/steven-matison/dfhz_hue_mpack)
