[Sage_CI_HL]: https://raw.githubusercontent.com/sagecontinuum/sage/master/resources/images/SAGE_CI.jpg "Sage CI Arch" 
## Overview
![Figure 1: A high-level overview of the Sage Cyber-infrastructure][Sage_CI_HL]

### Nodes:

#### Sage Node:  
Any Edge node part of the Sage project.  This includes new AoT nodes, Wild Sage nodes, and Sage Blades.
 
#### [Waggle Node](https://github.com/waggle-sensor/waggle):  
This slang indicates that an AI@Edge computer is running the Waggle software stack.  It is similar to saying “It’s a Linux Box”.  The Linux box could be running a web server or a database, but is running the core Linux software stack.  “A Waggle Node” runs the Waggle encrypted and reliable messaging layers, configuration system, resilience components, adheres to the Waggle security model, provides the AI@Edge runtime libraries, and provides the resource management components to schedule and run Edge docker containers from the Edge Code Repository. 
 
#### [Array of Things (AoT) Node](https://arrayofthings.github.io/):  
A weatherized Waggle Node designed to be installed on a street pole in the city or mounted on exterior walls.  An AoT node usually includes a sensor pod that includes air quality sensors.  The device is also attractive for an urban setting. 
 
#### Wild Sage Node:  
This identifies Waggle Nodes that are weatherized for remote, outdoor deployment as part of the Sage project.  These nodes are similar to AoT nodes, but since urban aesthetics are not needed, and different cameras and sensors might be used, the Wild Sage Node may look strange.  Wild Sage Nodes look like proper bits of science experiments mounted outside, while AoT nodes look like they deserve an architectural award. 
 
#### Sage Blade: 
This identifies Waggle Nodes that are standard, commercially available blade server or box intended for use in a machine room or climate controlled telecommunications hut.  For the Sage project, the first Sage Blades are Dell XR2 1U servers that have been hardened for increased environmental range. They include a powerful NVIDIA GPU for AI@Edge compute jobs.  As a Waggle Node, they run the complete Waggle software stack, and therefore can run Edge jobs, report data, and be remotely configured.

### Data and Code Repositories: 

#### Sage Data Repository (SDR): 
Sage data is made open for research wherever possible.  Some training data sets may require data-usage agreements to adhere to privacy guidelines or for operational security.  However all sensor data and AI@Edge inference results are intended to be open and immediately shared in near-real time via the SDR. The SDR aggregates all data collected by Sage Nodes and provides web-based tools for extracting (slicing and dicing) relevant data components or viewing the data on map tools.  (ex BDR)
 
#### [Edge Code Repository (ECR)](https://github.com/sagecontinuum/ecr): 
A library of tested and benchmarked AI@Edge codes that can run on the Waggle software stack.  The ECR provides a verified and versioned repository of AI@Edge docker images that can be pushed by the Beehive to Sage Nodes and executed.


### Sage Tools:

#### [Sage Edge Scheduler (SES)](https://github.com/sagecontinuum/ses):  
A single point of entry for requesting AI@Edge cyberinfrastructure resources.  Similar to how computer users see a batch schedule, the SES is the outward facing interface for submitting AI@Edge jobs, such as “evaluate overhead clouds”, “identify wildfire smoke”, or “count pedestrians”. 

### Support Infrastructure:
 
#### [Cloud Training Software Stack (CTSS)](https://github.com/sagecontinuum/ctss): 
CTSS will provide interfaces (CTSS Training Environment and CTSS API Client) and documentation with end-to-end examples for users to allow them to build and bundle the components necessary to test on a Virtual Waggle and then on a Sage Node. It can be run on the cloud or as a downloadable software.

#### [Chameleon](https://www.chameleoncloud.org/): 
A large-scale, deeply reconfigurable experimental platform built to support Computer Sciences systems research. Community projects range from systems research developing new operating systems, virtualization methods, performance variability studies, and power management research to projects in software defined networking, artificial intelligence, and resource management.

### Utilities:

#### [Virtual Waggle (VW)](https://github.com/sagecontinuum/vw): 
Virtual Waggle is a downloadable software-only programming environment for building and testing edge computing code for the Waggle framework. 
