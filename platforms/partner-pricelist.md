# Purchasing and Deploying Sage Nodes for Research Parnters

To deploy your own Sage system, four parts are
needed:

1.  **Sage Nodes** — Edge
    computers for in situ AI processing.
2.  **Sensors** — What does your science need?
3.  **Beehive Cloud Service** — Storage, data management, and software updates for Sage Nodes
4.  **Networking** — Mobile broadband, Starlink, wired, or WiFi networking

Each component is priced separately, based on your scientific needs. The <a
href="https://naise.northwestern.edu">Northwestern University / Argonne Institute for Science and Engineering (NAISE)</a> is the endpoint for purchasing contracts. The sum of all four pieces provides the total cost.  Installation costs must be budgeted as well, and may require permits or installation contractors. For many installations, students or scientific staff can perform the needed work. However, for urban and tower deployments, special installation procedures may be required. Ask the Sage team for guidance estimating your installation costs – every installation is different.  The data below will help scientists do basic planning before working with the Sage team to
construct a specific configuration.

## Definitions:

-  **Sage Node**:  A specially configured Linux server for running AI at the edge (AI@Edge) computing jobs with the Sage software stack.  A Sage Node is either a *Wild Sage Node* or a *Sage Blade*.

- **Wild Sage Node (WSN)**: A weatherized AI@Edge Linux node with extreme resilience features and support for attached power-over-ethernet (PoE) and USB sensors. Currently, the AI processor is an NVIDIA Jetson NX.

- **Sage Blade (SB)**:  A server with robust remote management features, such as the Dell iDrac or HPE iLO. Often, extended environmental range (temperature and humidity) is desired.  The AI processor could be an NVIDIA PCIe accelerator, or similar.

- **Beehive Cloud Service**: The backend data and management cloud service operated by the Northwestern University Sage team.  It provides a data archive, job scheduling, data access APIs, cybersecurity, and software maintenance updates and AI framework upgrades to nodes.

## Sage Node:

A *Wild Sage Node* or a *Sage Blade* is needed to run the Sage software stack at the edge and connect to sensors.  Wild Sage Nodes must be purchased from NAISE via a contract with Northwestern University, a non-profit university.  The Sage Blade is a simple Dell server, designed to be hosted in climate-controlled instrumentation huts or office space, and can be purchased directly from Dell. 

<table>
<colgroup>
<col style="width: 15%">
<col style="width: 75%">
<col style="width: 15%">
</colgroup>
<tbody>
<tr>
<td colspan="3">Sage
Node</td>
</tr>
<tr>
<td>Type</td>
<td>Features</td>
<td>2024 Cost</td>
</tr>
<tr>
<td><a
href="https://sagecontinuum.org/docs/installation-manuals/wsn-manual">Wild Sage Node</a></td>
<td>Ruggedized AI@Edge platform suitable
for mounting outside, across a wide range of temperatures.  Includes a
standard set of cameras and sensors (see table "WSN Sensors & Networking" below)</td>
<td>$10,100</td>
</tr>
<tr>
<td>Sage Blade</td>
<td>Rackmounted server with NVIDIA GPU
for AI@Edge workloads.  Robust remote management (iDRAC) supports deployment in remote instrument or networking huts.  Educational discounts vary.</td>
<td>~$6500</td>
</tr>
</tbody>
</table>

## Sensors:

Sage is designed to be expandable, so scientists can
attach their own sensors.  There is a growing list of sensors for which
the Sage team or Open Source contributors have already developed a
“plugin” which runs on a Sage Node and can collect data from a local
sensor for AI@Edge processing.  Teams can also use the excellent online documentation to integrate their own sensors and write a sensor plugin.  The following sensors are currently supported, with plugins that can pull data from
the sensor for in situ analysis on a Sage Node.

Depending on scientific goals, a Sage deployment might include several *user installed* sensors connected to each Sage Node.  The table below provides a list of some of the common additional sensors that can be easily attached.  The expensive sensors are not required, but demonstrate that Sage has integrated a wide range of the highest quality sensors, from simple camera and particulate sensors to radar and lidar.

<table>
<colgroup>
<col style="width: 25%">
<col style="width: 55%">
<col style="width: 15%">
</colgroup>
<tbody>
<tr>
<td colspan="3">User Installed
Sensors (at deployment site)</td>
</tr>
<tr>
<td>Sensor</td>
<td>Features</td>
<td>Sensor Cost</td>
</tr>
<tr>
<td><a
href="https://store.vaisala.com/en/products/WXT530">Vaisala WXT530</a></td>
<td>Provides high quality barometric
pressure, temperature, relative humidity, rainfall, wind speed and
direction measurements.</td>
<td>$3,200</td>
</tr>
<tr>
<td><a
href="https://www.vaisala.com/en/products/weather-environmental-sensors/air-quality-transmitter-aqt530-urban-industrial-systems">Vaisala AQT530</a></td>
<td>Provides observations on
meteorological conditions, including particulate matter (PM2.5, PM10)
and gas species concentrations (NO, NO2, O3, CO).</td>
<td>$3,500</td>
</tr>
<tr>
<td><a
href="https://metone.com/products/es-642/">MetOne ES-642</a></td>
<td>Detects 0.5 to 10 micron particles
using forward scatter laser nephelometer</td>
<td>$3,500</td>
</tr>
<tr>
<td><a
href="https://hanwhavisionamerica.com/product/xnp-6400rw/">Hanwha XNP-6400RW</a></td>
<td>Continuous PTZ Optical
Camera</td>
<td>$4,000</td>
</tr>
<tr>
<td><a
href="https://www.mobotix.com/en/products/outdoor-cameras/m16-allrounddual">Mobotix MX-M16TB-R079IP</a></td>
<td>Thermal and Optical dual eye camera
on PT mount</td>
<td>$10,000</td>
</tr>
<tr>
<td><a
href="https://metek.de/product/mrr-pro/">Micro Rain Radar MMR-PRO</a></td>
<td>Vertically pointing Ka-band Radar
that detects precipitation in a vertical column.</td>
<td>~$48,000</td>
</tr>
<tr>
<td><a
href="https://www.vaisala.com/en/products/weather-environmental-sensors/ceilometer-CL61-meteorology">Vaisala CL61</a></td>
<td>Lidar Ceilometer with depolarization
is designed for cloud height reporting and improved vertical
aerosol profiling.</td>
<td>~$50,000</td>
</tr>
<tr>
<td><a
href="https://halo-photonics.com/lidar-systems/stream-line-series/">Halo Streamline XR</a></td>
<td>Doppler LiDAR with  high
resolution, high output power – a range of ~10km.</td>
<td>~$250,000</td>
</tr>
<tr>
<td><a href="https://www.licor.com/env/products/eddy-covariance/LI-7500DS.html">LI-COR 7500DS + Accessories</a></td>
<td>Open Path CO2/H2O Analyzer designed for high-speed measurements in ambient air for eddy covariance computations along with 3D sonic anemometer.</td>
<td>~$24000</td>
</tr>
<tr>
<td><a
href="https://metek.de/product/usonic-3-class-a/">METEK uSonic-3 3D Ultrasonic Anemometer</a> </td>
<td>Provides observations of three
wind components (U, V, W) and acoustic temperature at a sampling rate of
up to 50 Hz, with heater for cold weather.</td>
<td>~$11,000</td>
</tr>
<tr> 
<td><a href="https://gillinstruments.com/wp-content/uploads/2022/08/WindMaster-Pro-iss-8.pdf">Gill WindMaster Pro 3D Ultrasonic Anemometer</a></td>
<td> Monitors wind speeds of 0-65m/s and provides
sonic temperature, speed of sound and U, V & W vector outputs at 32Hz.</td>
<td>~$4000</td>
</tr>
</tbody>
</table>


For Wild Sage Nodes, some optional components
must be integrated at the time the nodes are assembled and tested
by the electronics company for Northwestern University.  The table below
provides a list of sensors and additional networking components that can
be added to Wild Sage Nodes at the time of purchase.  For example, the
Ouster OS0 LiDAR, shown in the table below, might work best mounted
directly to a WSN for urban deployments.

<table>
<colgroup>
<col style="width: 25%">
<col style="width: 55%">
<col style="width: 15%">
</colgroup>
<tbody>
<tr>
<td colspan="3">WSN Sensors &amp;
Networking (must be integrated at factory)</td>
</tr>
<tr>
<td>Component</td>
<td>Features</td>
<td>Cost</td>
</tr>
<tr>
<td>Up-facing (cloud) <a
href="https://hanwhavisionamerica.com/product/xnf-8010rv/">XNF-8010RV</a> camera &amp;
down-facing (horizon) <a
href="https://hanwhavisionamerica.com/product/xnv-8081z/">XNV-8081Z</a> camera</td>
<td>WSNs support a wide range of
standard-mount cameras.  Upgraded cameras, such as the Hanwha:
XNV-8082R or XNV-8080 cost more, and could be
added.</td>
<td>Included in WSN
price</td>
</tr>
<tr>
<td>Integrated sensing capabilities for
Wild Sage Node</td>
<td>GPS, Rainfall Sensor> (<a href="https://rainsensors.com/products/rg-15">rg-15</a>), microphone,
atmospheric pressure and humidity, temperature sensors (<a
href="https://www.bosch-sensortec.com/products/environmental-sensors/gas-sensors/bme680/">bme 680</a>)</td>
<td>Included in WSN
price</td>
</tr>
<tr>
<td><a
href="https://ouster.com/products/scanning-lidar/os0-sensor/">Ouster OS0 LiDAR</a></td>
<td>Ultra-wide 90° field of view digital
lidar sensor</td>
<td>$9500</td>
</tr>
<tr>
<td><a
href="https://www.rakwireless.com/en-us/products/lpwan-gateways-and-concentrators/rak2287-sx1302">RAK2287</a></td>
<td>LoRaWAN RPi Gateway</td>
<td>$600</td>
</tr>
<tr>
<td><a
href="https://www.rtl-sdr.com">RTL-SDR</a></td>
<td>Software Defined Radio: provides
lightning detection, RF spectrum analysis, etc.</td>
<td>$100</td>
</tr>
<tr>
<td>Broadband Modem</td>
<td>Cellular (LTE) for
networking</td>
<td>$300</td>
</tr>
</tbody>
</table>


## Beehive Cloud Service:

All Sage Nodes (Wild Sage Nodes and Sage Blades) need
access to the managed cloud storage service,
Beehive.  The <a href="https://portal.sagecontinuum.org/">Sage web portal</a>
includes job scheduler, data browser, and live data
access APIs.  The Sage team manages the Beehive cloud service and
provides teams access to the web-based management portal. Beehive also
manages cybersecurity and software updates, such as new AI libraries, to
deployed nodes.

The table below provides the cost per year, per node, for
the Beehive Cloud Service.  Larger deployments are more economical because
management operations and configuration changes are often shared across a given set of deployed nodes.

<table>
<colgroup>
<col style="width: 20%">
<col style="width: 80%">
</colgroup>
<tbody>
<tr class="odd c25">
<td class="c23">Deployment size
(nodes)        </td>
<td class="c17">2024 Cost/year/node</td>
</tr>
<tr class="even c25">
<td class="c23">1</td>
<td class="c17">$32.0K</td>
</tr>
<tr class="odd c41">
<td class="c23">5</td>
<td class="c17">$29.0K</td>
</tr>
<tr class="even c25">
<td class="c23">10</td>
<td class="c17">$25.0K</td>
</tr>
<tr class="odd c25">
<td class="c23">20</td>
<td class="c17">$21.8K</td>
</tr>
<tr class="even c25">
<td class="c23">30</td>
<td class="c17">$20.1K</td>
</tr>
<tr class="odd c25">
<td class="c23">50</td>
<td class="c17">$18.8K</td>
</tr>
</tbody>
</table>



## Networking & Data Transfer

Networking and data transfer, for example cellular broadband LTE or
Starlink, should also be budgeted, and depends on local wireless
providers and their pricing.  WSNs not directly connected via wired
Ethernet or Starlink, will likely need an broadband LTE modem or Wifi connection
installed during manufacturing (see table above).

## Worked Example

Given the costs above, here are some worked
examples:

**Example A**:  A single WSN with additional Mobotix Infrared sensor connected to a Pan/Tilt platform:

Sensors: \$10,000 (Mobotix)

WSN: \$10,100 (node) + \$300 (Broadband LTE Modem) = \$10,400

Beehive Cloud Service: \$32,000/yr

Broadband Networking Data Plan for WSNs: \$480/yr

So the total for the first year would be: \$52,880 (equipment purchase + Beehive and broadband)

Additional years would be \$32,480 (Beehive and broadband cost)

**Example B**:  A 20 node deployment: 10 WSN and 10 Sage Blades, each with an Air Quality sensor. Also, there are two Micropulse Radars (assuming \$25k each). Assume networking for Wild Sage Nodes is provided by LTE broadband; Sage Blades are hard wired to the non-metered and zero cost Internet infrastructure.

Sensors: \$3,500 (MetOne) \* 20  + \$25,000 (micropulse radar) \* 2 = \$120,000

WSN: (\$10,100 (node) + \$300 (Broadband LTE Modem)) \* 10 = \$104,000

Sage Blade: \$6,500 \* 10 = \$65,000

Beehive Cloud Service: \$21,800 \* 20 = \$463,000

Broadband Networking Data Plan for WSNs: \$480/yr \* 10 = \$4,800

So the total for the first year would be: \$756,800 (equipment plus Beehive and broadband).

Additional years would be \$468,800 (Beehive and broadband cost)

For a 3 year project, the total for a 20 node deployment with Sage nodes and the sensors described above: \$1,694,400.

Not included in this worksheet of pricing:

\* Shipping of WSN nodes from local electronics
manufacturing (Chicago area)

\* Installation of nodes at destination.
