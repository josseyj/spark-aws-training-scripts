training-scripts
================

Scripts to launch cluster used for Strata

## Command 
* Follow the instructions [here](http://ampcamp.berkeley.edu/big-data-mini-course/launching-a-bdas-cluster-on-ec2.html)
  * `./spark-ec2 -i ../sparklekey3.pem -k sparklekey3  launch amplab-training`
  * If fails `./spark-ec2 -i ../sparklekey3.pem -k sparklekey3 --resume  launch amplab-training`
  * ./spark-ec2 -i ../sparklekey3.pem -k sparklekey3 get-master amplab-training
  * Then ssh into the master
  * Run `spark/bin/spark-shell` on the master
  
  
## Troubleshooting

* `spark-shell` in the -master- throwing error `java.io.FileNotFoundException: /root/tachyon/target/tachyon-0.3.0-jar-with-dependencies.jar (No such file or directory)`
 * Run `./spark-ec2/tachyon/init.sh`
