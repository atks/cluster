cluster
=======

More help on: https://statgen.sph.umich.edu/wiki/Cluster_tools

Some useful tools for UM Statgen clusters

* ckill                     kills mosbatch jobs that are sleeping on the gateway and those active on the cluster nodes.
* cruns <usr>               sees jobs flagging <usr> which is default you running on a gateway that you are on right now.
* cusage                    sees jobs summarized by user on all gateways.
* ctop                      sees top output of a node.
* generate_good_node_list   generates list of nodes with the node number and its corresponding slurm name separated by a tab. 
* pick_main_node            picks a main node to use with the least jobs based on surveying fantasia/wonderland/snowwhite/slurm.
* pick_mini_node            picks a node to use on minicluster with 4 nodes.
* pick_mini+_node           picks a node to use on minicluster with 8 nodes.

pick_*_nodes are modified from Goo's original scripts.

A) To configure user, create a .config file in the program directory that has your user name.
   
1. Assume your user name is "atks". Go to the program directory.

   cd \<cluster-program-dir\>

2. Write file.

   echo "atks" > .config

B) You will need to generate a public/private RSA key pair 
and authorize the public key while having no passphrase
for the private key.

1. generate your private key and public key, make sure there is no passphrase for your private key.
  
   ssh-keygen

2. Concatenate your public key to .ssh/authorized_keys

   cat .ssh/id_rsa.pub >> .ssh/authorized_keys
   
   Note that your public key might be in some other file depending on the mode of your key generation. 
