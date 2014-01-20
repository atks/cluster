cluster
=======

Some useful tools for UM Statgen clusters

You will need to generate a public/private RSA key pair 
and authorize the public key while having no passphrase
for the private key.

ckill                     kills mosbatch jobs that are sleeping on the gateway and those active on the cluster nodes.

cruns                     sees jobs running on a gateway that you are on right now.

cusage                    sees jobs summarized by user on all gateways.

generate_good_node_list   generates list of nodes with the node number and its corresponding slurm name separated by a tab. 

pick_main_node            picks a main node to use with the least jobs based on surveying fantasia/wonderland/snowwhite/slurm.

pick_mini_node            picks a node to use on minicluster with 4 nodes.

pick_mini+_node           picks a node to use on minicluster with 8 nodes.


* pick_*_nodes are modified from Goo's original scripts.
