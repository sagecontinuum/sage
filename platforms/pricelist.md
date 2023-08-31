# Purchasing and Deploying Sage Nodes

To deploy your own Sage system, four parts are
needed:

1.  **Sage Nodes** — edge
    computers for in situ AI processing.
2.  **Sensors** — what does your science need?
3.  **Beehive Cloud Service** — storage and data management for Sage Nodes
4.  **Networking** — mobile broadband, Starlink, wired, or WiFi networking

Each component is priced separately, based on your scientific
needs.  The sum of all four pieces provides the total cost you should
budget.  You should plan for installation as well.  For many
installations, students or scientific staff can perform the needed work.  However, for urban and tower deployments, special installation procedures might be
required. Ask the Sage team for guidance estimating your installation
costs – every installation is different.  The data below will help
scientists do basic planning before working with the Sage team to
construct a specific configuration.

## Definitions:

-  **Sage Node**:  A specially configured Linux server for running AI at the edge (AI@Edge) computing jobs with the Sage software stack.  A Sage Node is either a *Wild Sage Node* or a *Sage Blade*.

- **Wild Sage Node (WSN)**: A weatherized AI@Edge Linux node with extreme resilience features and support for attached power-over-ethernet (PoE) and USB sensors. Currently, the AI processor is an NVIDIA Jetson NX.

- **Sage Blade (SB)**:  A Dell server with robust remote management features (iDRAC) and often extended environmental range (temperature and humidity). The AI processor is an NVIDIA T4 or similar accelerator.

- **Beehive Cloud Service**: The backend data and management cloud service operated by the Sage team.  It provides a data archive, job scheduling, data access APIs, cybersecurity, and software maintenance updates and AI framework upgrades to nodes.

## Sage Node:

A *Wild Sage Node* or a *Sage Blade* is needed to run the Sage software stack at the edge and connect to sensors.  Wild Sage Nodes must be purchased from Northwestern University via a contract with the Sage team at the <a
href="https://naise.northwestern.edu">Northwestern University / Argonne Institute for Science and Engineering (NAISE)</a>.  The Sage Blade is a simple Dell server, designed to be hosted in climate-controlled instrumentation huts or office space, and can be purchased directly from Dell. 

<table>
<colgroup>
<col style="width: 15%">
<col style="width: 75%">
<col style="width: 15%">
</colgroup>
<tbody>
<tr>
<td colspan="3"><p>Sage
Node</p></td>
</tr>
<tr>
<td><p>Type</p></td>
<td><p>Features</p></td>
<td><p>Cost</p></td>
</tr>
<tr>
<td><p><a
href="https://sagecontinuum.org/docs/installation-manuals/wsn-manual">Wild Sage Node</a></p></td>
<td><p>Ruggedized AI@Edge platform suitable
for mounting outside, across a wide range of temperatures.  Includes a
standard set of cameras and sensors (see table "WSN Sensors & Networking" below)</p></td>
<td><p>$9500</p></td>
</tr>
<tr>
<td><p>Sage Blade</p></td>
<td><p>Rackmounted server with NVIDIA GPU
for AI@Edge workloads.  Robust remote management (iDRAC) supports deployment in remote instrument or networking huts.  Educational discounts vary.</p></td>
<td><p>~$6500</p></td>
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
<td colspan="3"><p>User Installed
Sensors (at deployment site)</p></td>
</tr>
<tr>
<td>Sensor</td>
<td>Features</td>
<td>Cost</td>
</tr>
<tr>
<td><p><a
href="https://store.vaisala.com/en/products/WXT530">Vaisala WXT530</a></p></td>
<td><p>Provides high quality barometric
pressure, temperature, relative humidity, rainfall, wind speed and
direction measurements.</p></td>
<td><p>$3,200</p></td>
</tr>
<tr>
<td><p><a
href="https://www.vaisala.com/en/products/weather-environmental-sensors/air-quality-transmitter-aqt530-urban-industrial-systems">Vaisala AQT530</a></p></td>
<td><p>Provides observations on
meteorological conditions, including particulate matter (PM2.5, PM10)
and gas species concentrations (NO, NO2, O3, CO).</p></td>
<td><p>$3,500</p></td>
</tr>
<tr>
<td><p><a
href="https://metone.com/products/es-642/">MetOne ES-642</a></p></td>
<td><p>Detects 0.5 to 10 micron particles
using forward scatter laser nephelometer</p></td>
<td><p>$3,500</p></td>
</tr>
<tr>
<td><p><a
href="https://hanwhavisionamerica.com/product/xnp-6400rw/">Hanwha XNP-6400RW</a></p></td>
<td><p>Continuous PTZ Optical
Camera</p></td>
<td><p>$4,000</p></td>
</tr>
<tr>
<td><p><a
href="https://www.mobotix.com/en/products/outdoor-cameras/m16-allrounddual">Mobotix MX-M16TB-R079IP</a></p></td>
<td><p>Thermal and Optical dual eye camera
on PT mount</p></td>
<td><p>$10,000</p></td>
</tr>
<tr>
<td><p><a
href="https://metek.de/product/usonic-3-class-a/">METEK uSonic-3 3D Ultrasonic Anemometer</a> </p></td>
<td><p>Provides observations of three
wind components (U, V, W) and acoustic temperature at a sampling rate of
up to 50 Hz, with heater for cold weather.</p></td>
<td><p>~$11,000</p></td>
</tr>
<tr>
<td><p><a
href="https://metek.de/product/mrr-pro/">Micro Rain Radar MMR-PRO</a></p></td>
<td><p>Vertically pointing Ka-band Radar
that detects precipitation in a vertical column.</p></td>
<td><p>~$48,000</p></td>
</tr>
<tr>
<td><p><a
href="https://www.vaisala.com/en/products/weather-environmental-sensors/ceilometer-CL61-meteorology">Vaisala CL61</a></p></td>
<td><p>Lidar Ceilometer with depolarization
is designed for cloud height reporting and improved vertical</p>
<p>aerosol profiling.</p></td>
<td><p>~$50,000</p></td>
</tr>
<tr>
<td><p><a
href="https://halo-photonics.com/lidar-systems/stream-line-series/">Halo Streamline XR</a></p></td>
<td><p>Doppler LiDAR with  high
resolution, high output power – a range of ~10km.</p></td>
<td><p>~$250,000</p></td>
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
<td colspan="3"><p>WSN Sensors &amp;
Networking (must be integrated at factory)</p></td>
</tr>
<tr>
<td><p>Component</p></td>
<td><p>Features</p></td>
<td><p>Cost</p></td>
</tr>
<tr>
<td><p>Up-facing (cloud) <a
href="https://hanwhavisionamerica.com/product/xnf-8010rv/">XNF-8010RV</a> camera &amp;
down-facing (horizon) <a
href="https://hanwhavisionamerica.com/product/xnv-8081z/">XNV-8081Z</a> camera</p></td>
<td><p>WSNs support a wide range of
standard-mount cameras.  Upgraded cameras, such as the Hanwha:
XNV-8082R or XNV-8080 cost more, and could be
added.</p></td>
<td><p>Included in WSN
price</p></td>
</tr>
<tr>
<td><p>Integrated sensing capabilities for
Wild Sage Node</p></td>
<td><p>GPS, Rainfall Sensor> (<a href="https://rainsensors.com/products/rg-15">rg-15</a>), microphone,
gas,pressure, humidity and temperature sensors (<a
href="https://www.bosch-sensortec.com/products/environmental-sensors/gas-sensors/bme680/">bme 680</a>)</p></td>
<td><p>Included in WSN
price</p></td>
</tr>
<tr>
<td><p><a
href="https://ouster.com/products/scanning-lidar/os0-sensor/">Ouster OS0 LiDAR</a></p></td>
<td><p>Ultra-wide 90° field of view digital
lidar sensor</p></td>
<td><p>$9500</p></td>
</tr>
<tr>
<td><p><a
href="https://www.rakwireless.com/en-us/products/lpwan-gateways-and-concentrators/rak2287-sx1302">RAK2287</a></p></td>
<td><p>LoRaWAN RPi Gateway</p></td>
<td><p>$600</p></td>
</tr>
<tr>
<td><p><a
href="https://www.rtl-sdr.com">RTL-SDR</a></p></td>
<td><p>Software Defined Radio: provides
lightning detection, RF spectrum analysis, etc.</p></td>
<td><p>$100</p></td>
</tr>
<tr>
<td><p>Broadband Modem</p></td>
<td><p>Cellular (LTE) for
networking</p></td>
<td><p>$300</p></td>
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

The table below shows the price per year, per node, for
the Beehive Cloud Service.  Larger deployments are more economical.

<table>
<colgroup>
<col style="width: 20%">
<col style="width: 80%">
</colgroup>
<tbody>
<tr class="odd c25">
<td class="c23"><p>Deployment size
(nodes)        </p></td>
<td class="c17"><p>Cost/year/node</p></td>
</tr>
<tr class="even c25">
<td class="c23"><p>1</p></td>
<td class="c17"><p>$16.7K</p></td>
</tr>
<tr class="odd c41">
<td class="c23"><p>5</p></td>
<td class="c17"><p>$13.3K</p></td>
</tr>
<tr class="even c25">
<td class="c23"><p>10</p></td>
<td class="c17"><p>$9.8K</p></td>
</tr>
<tr class="odd c25">
<td class="c23"><p>20</p></td>
<td class="c17"><p>$8.3K</p></td>
</tr>
<tr class="even c25">
<td class="c23"><p>30</p></td>
<td class="c17"><p>$7.7K</p></td>
</tr>
<tr class="odd c25">
<td class="c23"><p>50</p></td>
<td class="c17"><p>$7K</p></td>
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

WSN: \$9,500 (node) + \$300 (Broadband LTE Modem) = \$9,800

Beehive Cloud Service: \$16,700/yr

Broadband Networking Data Plan: \$480/yr

So the total for the first year would be: \$36,980 (equipment purchase + Beehive and broadband)

Additional years would be \$17,180 (Beehive and broadband cost)

**Example B**:  A 20 node deployment: 10 WSN and 10 Sage Blades, each with an Air Quality sensor. Also, there are two Micropulse Radars (assuming \$25k each). Assume networking for Wild Sage Nodes is provided by LTE broadband; Sage Blades are hard wired to the non-metered and zero cost Internet infrastructure.

Sensors: \$3,500 (MetOne) \* 20  + \$25,000 (micropulse radar) \* 2 = \$120,000

WSN: (\$9,500 (node) + \$300 (Broadband LTE Modem)) \* 10 = \$98,000

Sage Blade: \$6,500 \* 10 = \$65,000

Beehive Cloud Service: \$8,300 \* 20 = \$166,000

Broadband Networking Data Plan: \$480/yr \* 10 = \$4,800

So the total for the first year would be: \$453,800 (equipment plus Beehive and broadband).

Additional years would be \$170,800 (Beehive and broadband cost)

For a 3 year NSF grant, the total charged to the project for a 20 node deployment with Sage nodes and the sensors described above: \$792,400.

Not included in this worksheet of pricing:

\* Shipping of WSN nodes from local electronics
manufacturing (Chicago area)

\* Installation of nodes at destination.
