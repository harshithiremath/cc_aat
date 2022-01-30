# Task Scheduling with Deadline and Priority

Task Scheduling with Deadline and Priority Algorithm is a modified version of Earliest Deadline First (EDF).  
When the deadlines of two processes/tasks are the same, then the priority is used to decide which one to execute first - the one with high priority (less numeric value) is executed first.  
Pseudo-algorithm

```
If p1.deadline != p2.deadline:
    if (p1.deadline < p2.deadline)
        do P1 first;
    else
        do P2 first;
else:
    if (p1.priority <= p2.priority)
        do P1 first;
    else
        do P2 first;
```

To run this using CloudSim:

1. Install [CloudSim](https://github.com/Cloudslab/cloudsim/releases)
2. Using the files in this repo, replace the following files
    - **_Cloudlet.java_** in `cloudsim/modules/cloudsim/src/main/java/org/cloudbus/cloudsim`
    - **_DatacenterBroker.java_** in `cloudsim/modules/cloudsim/src/main/java/org/cloudbus/cloudsim` - Function [_submitCloudlets_](https://github.com/harshithiremath/cc_aat/blob/1f0a5098814596bfa9327aa52ebfaa9498f1c639/DatacenterBroker.java#L335-L391) in this file is where the actual algorithm runs
    - **_Simulation.java_** in `cloudsim/modules/cloudsim-examples/src/main/java/org/cloudbus/cloudsim/examples`
3. Compile and run.
