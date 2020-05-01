## The big Picture

Here..

## Terminology

### [Waggle Node](https://github.com/waggle-sensor/waggle):  

This slang indicates that an AI@Edge computer is running the Waggle software stack.  It is like saying “It’s a Linux Box”.  That Linux box could be running a web server or a database, but is running the Linux software stack.  “A Waggle Node” runs the Waggle encrypted and reliable messaging layers, configuration system, recovery components, adheres to the Waggle security model, provides the AI@Edge runtime libraries, and provides a the resource management components to schedule and run Edge docker containers from the Edge Code Repository. 

### [Array of Things (AoT) Node](https://arrayofthings.github.io/):  
A weatherized Waggle Node designed to be installed on a street pole in the city or mounted on exterior walls.  An AoT node usually includes a sensor pod that includes air quality sensors.  The device is also attractive for an urban setting. 

### Wild Sage Node:  
This identifies Waggle Nodes that are weatherized for remote, outdoor deployment as part of the Sage project.  These nodes are similar to AoT nodes, but since urban aesthetics are not needed, and different cameras and sensors might be used, the Wild Sage Node may look strange.  Wild Sage Nodes look like proper bits of science experiments mounted outside, while AoT nodes look like they deserve an architectural award. 

### Sage Data Repository: 
This is a data-repository that is hosted at UCSD. The public gets all sage data from this repository. 

### Sage Blade: 
This identifies Waggle Nodes that are standard, commercially available blade server or box intended for use in a machine room or climate controlled telecommunications hut.  For the Sage project, the first Sage Blades are Dell XR2 1U servers that have been hardened for increased environmental range. They include a powerful NVIDIA GPU for AI@Edge compute jobs.  As a Waggle Node, they run the complete Waggle software stack, and therefore can run Edge jobs, report data, and be remotely configured.

### Sage Node: 
Any Edge node part of the Sage project.  This includes new AoT nodes, Wild Sage nodes, and Sage Blades.

### [Beehive](https://github.com/waggle-sensor/beehive-server): 
A set of secure servers that manage Sage Nodes.  Beehive collects CPU/GPU performance data and forwards sensor data and AI@Edge inference results to the Sage Data Repository.  Beehive also provides digital certificates for each Sage Node, updates configurations, and archives communications from and to Sage Nodes.  Beehive pushes AI@Edge user codes to Sage Nodes based on the Sage Edge Scheduler. 

### [Edge Code Repository (ECR)](https://github.com/sagecontinuum/ecr): 
A library of tested and benchmarked AI@Edge codes that can run on the Waggle software stack.  The ECR provides a verified and versioned repository of AI@Edge docker images that can be pushed by the Beehive to Sage Nodes and executed.


### [Sage Edge Scheduler (SES)](https://github.com/sagecontinuum/ses):  
A single point of entry for requesting AI@Edge cyberinfrastructure resources.  Similar to how computer users see a batch schedule, the SES is the outward facing interface for submitting AI@Edge jobs, such as “evaluate overhead clouds”, “identify wildfire smoke”, or “count pedestrians”. 


### [Virtual Waggle (VW)](https://github.com/sagecontinuum/vw): 
... 

### [Cloud Training Software Stack(CTSS)](https://github.com/sagecontinuum/ctss): 
CTSS will provide interfaces (CTSS Training Environment and CTSS API Client) and documentation with end-to-end examples for users to allow them to build and bundle the components necessary to test on a Virtual Waggle and then on a Sage Node. It can be run on the cloud or as a downloadable software

