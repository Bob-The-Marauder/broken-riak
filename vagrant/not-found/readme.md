This Vagrant file spawns 5 Riak KV instances, creates a cluster, adds a round robin load balancer and then adds sample data via the load balancer.

After using this cluster for a while, it becomes apparent that some read requests are receiving "Not found" errors on occasion but performing the same operation again later returns normally. Pull riak-debugs from each node and investigate.

For convenience, VMs are labelled riak1 throught to riak5 e.g. "vagrant ssh riak3" would log you in to the third Riak KV instance. The load balancer is located on riak5 and is listening on port 80.
