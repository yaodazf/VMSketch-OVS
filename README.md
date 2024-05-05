#VMSketch-CPU

Our source code consists of five files, where File "GeneralHash.cpp" implements the functionality of the hash function, and File "kPersistent.cpp" implements the pseudocode from the paper. Specifically, the function HashTableInsert in File "kPersistent.cpp" implements the recording process for each element of flows, while the function EstimatedKSpread in File "kPersistent.cpp" implements the spread query functionality for any given flow.

#VMSketch-OVS

This repository includes a part of ovs, it cannot compile unless it is put in the ovs directory. This repository was made only for convenient, to prevent cloning the entire ovs repo and load them to the code editor. Compilation environment is ubuntu 16.04 and openvswitch-2.10.2. The VMSketch is integrated into the file datapath.c.

#VMSketch-DPDK

This repository includes a part of DPDK-20.11-stable version, it cannot compile unless it is put in the DPDK directory. This repository was made only for convenient, to prevent cloning the entire DPDK repo and load them to the code editor. In a nutshell, VMSketch achieves flow cardinality monitoring at nearly 14.88Mpps (i.e., 10 Gpbs line rate fully loaded with minimum size packets, 64B) with negligible packet losses (just a few packets per million) using a minimal amount of CPU resources.

Our VMSketch test is based on I/O mode of testpmd. Please replace the files in the origional folder testpmd with our version, which includes codes of VMSketch. Then, compile the whole DPDK following the standard installation process of DPDK. Last, the VMSketch test can be done with a line rate packet generator (e.g., PktGen-21.03.0 in our experiment).
