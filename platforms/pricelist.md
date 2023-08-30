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
installations, students can perform the needed work.  However, for urban
and tower deployments, special installation procedures might be
required. Ask the Sage team for guidance estimating your installation
costs – every installation is different.  The data below will help
scientists do basic planning before working with the Sage team to
construct a specific configuration.

## Definitions:

-  **Sage Node**:  A specially configured Linux server for running AI at the edge (AI@Edge) computing jobs on the Sage software stack.  A Sage Node is either *Wild Sage Node* or a *Sage Blade*.

- **Wild Sage Node (WSN)**: A weatherized AI@Edge Linux node with extreme resilience features and support for attached power-over-ethernet (PoE) and USB sensors. Currently, the AI processor is an NVIDIA Jetson NX.

- **Sage Blade (SB)**:  A Dell server with robust remote management features (iDRAC) and often extended environmental range (temperature and humidity). The AI processor is an NVIDIA T4 or similar accelerator.

- **Beehive Cloud Service**: The backend data and management cloud service operated by the Sage team.  It provides a data archive, job scheduling, data access APIs, cybersecurity, and software maintenance updates and AI framework upgrades to nodes.

## Sage Node:

A *Wild Sage Node* or a *Sage Blade* is needed to run the Sage software stack at the edge and connect to sensors.  Wild Sage Nodes must be purchased from Northwestern University via a contract with the Sage team at the <a
href="https://naise.northwestern.edu">Northwestern University / Argonne Institute for Science and Engineering (NAISE)</a>.  The Sage Blade is a simple Dell server, designed to be hosted in climate-controlled instrumentation huts or office space, and can be purchased directly from Dell. 

<span id="t.d5d3903c31cf31288f4c05274eb8978a9cc21e6e"></span><span id="t.0"></span>

<table>
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
<tr class="odd c18">
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
card for AI@Edge workloads.  Dell product line provides robust iDRAC
remote management features for deployment in remote instrument or
networking huts.  Educational discounts may vary.</p></td>
<td><p>~ $6500</p></td>
</tr>
</tbody>
</table>

<span class="c22 c37 c47"></span>

## Sensors:

Sage is designed to be expandable, so scientists can
attach their own sensors.  There is a growing list of sensors for which
the Sage team or Open Source contributors have already developed a
“plugin” which runs on a Sage Node and can collect data from a local
sensor.  Teams can also use the excellent online documentation to
integrate their own sensors and write a sensor plugin.  The following
sensors are currently supported, with plugins that can pull data from
the sensor for in situ analysis on a Sage Node.

Depending on scientific goals, a Sage deployment might include several *user installed* sensors added to each Sage node.  The table below provides a list of some of the common additional sensors that can be connected to a Sage Node.  The extremely expensive sensors are not required, but demonstrate that Sage has integrated a wide range of the highest quality sensors, from simple camera and particulate sensors to radar and lidar.

<span id="t.1312035281afa2d8e51b73c49f5c77ef2f330538"></span><span id="t.1"></span>

<table class="c28">
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd c18">
<td colspan="3" class="c43"><p><span class="c22 c21">User Installed
Sensors (at deployment site)</span></p></td>
</tr>
<tr class="even c18">
<td class="c19"><p><span class="c21">Sensor</span></p></td>
<td class="c11"><p><span class="c21">Features</span></p></td>
<td class="c30"><p><span class="c21">Cost</span></p></td>
</tr>
<tr class="odd c18">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://hanwhavisionamerica.com/product/xnp-6400rw/&amp;sa=D&amp;source=editors&amp;ust=1693388427192756&amp;usg=AOvVaw130FY-PuQDVLIdIKC_SPwh"
class="c9">Hanwha XNP-6400RW</a></span></p></td>
<td class="c11"><p><span class="c1">Continuous PTZ Optical
Camera</span></p></td>
<td class="c30"><p><span class="c1">$4,000</span></p></td>
</tr>
<tr class="even c18">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://www.mobotix.com/en/products/outdoor-cameras/m16-allrounddual&amp;sa=D&amp;source=editors&amp;ust=1693388427193468&amp;usg=AOvVaw1V-y8JB1QlJSqXN639WYVs"
class="c9">Mobotix MX-M16TB-R079IP</a></span></p></td>
<td class="c11"><p><span class="c1">Thermal and Optical dual eye camera
on PT mount</span></p></td>
<td class="c30"><p><span class="c1">$10,000</span></p></td>
</tr>
<tr class="odd c42">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://metone.com/products/es-642/&amp;sa=D&amp;source=editors&amp;ust=1693388427194144&amp;usg=AOvVaw0KX5XVBL6b7AZ9T5Eq6i9C"
class="c9">MetOne ES-642</a></span></p></td>
<td class="c11"><p><span class="c1">Detects 0.5 to 10 micron particles
using forward scatter laser nephelometer</span></p></td>
<td class="c30"><p><span class="c1">$3,500</span></p></td>
</tr>
<tr class="even c2">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://metek.de/product/mrr-pro/&amp;sa=D&amp;source=editors&amp;ust=1693388427194945&amp;usg=AOvVaw2m2UbxPOSM4aBrIo1LHiMz"
class="c9">Micro Rain Radar MMR-PRO</a></span></p></td>
<td class="c11"><p><span class="c15">Vertically pointing Ka-band Radar
that detects precipitation in a vertical column.</span></p></td>
<td class="c30"><p><span class="c1">~ $48,000</span></p></td>
</tr>
<tr class="odd c2">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://store.vaisala.com/en/products/WXT530&amp;sa=D&amp;source=editors&amp;ust=1693388427195730&amp;usg=AOvVaw0bRSrqrLdI8RzFeXUZIIT_"
class="c9">Vaisala WXT530</a></span></p></td>
<td class="c11"><p><span class="c1">Provides high quality barometric
pressure, temperature, relative humidity, rainfall, wind speed and
direction measurements.</span></p></td>
<td class="c30"><p><span class="c1">$3,200</span></p></td>
</tr>
<tr class="even c2">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://www.vaisala.com/en/products/weather-environmental-sensors/ceilometer-CL61-meteorology&amp;sa=D&amp;source=editors&amp;ust=1693388427196490&amp;usg=AOvVaw0tSQ1mjN7XpBAQXVU23YGR"
class="c9">Vaisala CL61</a></span></p></td>
<td class="c11"><p><span class="c1">Lidar Ceilometer with depolarization
is designed for cloud height reporting and improved vertical</span></p>
<p><span class="c1">aerosol profiling.</span></p></td>
<td class="c30"><p><span class="c1">~ $50,000</span></p></td>
</tr>
<tr class="odd c2">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://halo-photonics.com/lidar-systems/stream-line-series/&amp;sa=D&amp;source=editors&amp;ust=1693388427197314&amp;usg=AOvVaw19GjNGTPgNYT7sLPD4tycQ"
class="c9">Halo Streamline XR</a></span></p></td>
<td class="c11"><p><span class="c15">Doppler LiDAR with  high
resolution, high output power – a range of ~10km.</span></p></td>
<td class="c30"><p><span class="c1">~ $250,000</span></p></td>
</tr>
<tr class="even c2">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://www.vaisala.com/en/products/weather-environmental-sensors/air-quality-transmitter-aqt530-urban-industrial-systems&amp;sa=D&amp;source=editors&amp;ust=1693388427198147&amp;usg=AOvVaw3sekQjrdHQ89b3LU2zD9Y3"
class="c9">Vaisala AQT530</a></span></p></td>
<td class="c11"><p><span class="c15">Provides observations on
meteorological conditions, including particulate matter (PM2.5, PM10)
and gas species concentrations (NO, NO2, O3, CO).</span></p></td>
<td class="c30"><p><span class="c15">$3,500</span></p></td>
</tr>
<tr class="odd c2">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://metek.de/product/usonic-3-class-a/&amp;sa=D&amp;source=editors&amp;ust=1693388427198955&amp;usg=AOvVaw2jT4FVC8V_9dPojiM-g9Qj"
class="c9">METEK uSonic-3 3D Ultrasonic Anemometer</a></span><span
class="c1"> </span></p></td>
<td class="c11"><p><span class="c1 c40">Provides observations of three
wind components (U, V, W) and acoustic temperature at a sampling rate of
up to 50 Hz, with heater for cold weather.</span></p></td>
<td class="c30"><p><span class="c15">~ $11,000</span></p></td>
</tr>
</tbody>
</table>

<span class="c6"></span>

For Wild Sage Nodes, there are optional components
that must be integrated at the time the nodes are assembled and tested
by the electronics company for Northwestern University.  The table below
provides a list of sensors and additional networking components that can
be added to Wild Sage Nodes at the time of purchase.  For example, the
Ouster OS0 LiDAR, shown in the table below, might work best mounted
directly to a WSN for urban deployments.

<span id="t.e076e5ae5f42adb068cac2be871aa82abfd9066b"></span><span id="t.2"></span>

<table class="c28">
<tbody>
<tr class="odd c18">
<td colspan="3" class="c43"><p><span class="c22 c21">WSN Sensors &amp;
Networking (must be integrated at factory)</span></p></td>
</tr>
<tr class="even c18">
<td class="c19"><p><span class="c21">Component</span></p></td>
<td class="c32"><p><span class="c21">Features</span></p></td>
<td class="c29"><p><span class="c21">Cost</span></p></td>
</tr>
<tr class="odd c38">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://ouster.com/products/scanning-lidar/os0-sensor/&amp;sa=D&amp;source=editors&amp;ust=1693388427201620&amp;usg=AOvVaw3ZvZzQmD8kRRsJMavPwYx3"
class="c9">Ouster OS0 LiDAR</a></span></p></td>
<td class="c32"><p><span class="c1">Ultra-wide 90° field of view digital
lidar sensor</span></p></td>
<td class="c29"><p><span class="c1">$9500</span></p></td>
</tr>
<tr class="even c35">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://www.rakwireless.com/en-us/products/lpwan-gateways-and-concentrators/rak2287-sx1302&amp;sa=D&amp;source=editors&amp;ust=1693388427202732&amp;usg=AOvVaw26eoYDC5y8qSHC9Il4Fihl"
class="c9">RAK2287</a></span></p></td>
<td class="c32"><p><span class="c1">LoRaWAN RPi Gateway</span></p></td>
<td class="c29"><p><span class="c1">$600</span></p></td>
</tr>
<tr class="odd c35">
<td class="c33"><p><span class="c8"><a
href="https://www.google.com/url?q=https://www.rtl-sdr.com&amp;sa=D&amp;source=editors&amp;ust=1693388427203565&amp;usg=AOvVaw2eTPRC_j7X7gbGTpVsQ54I"
class="c9">RTL-SDR</a></span></p></td>
<td class="c32"><p><span class="c1">Software Defined Radio: provides
lightning detection, RF spectrum analysis, etc.</span></p></td>
<td class="c29"><p><span class="c1">$100</span></p></td>
</tr>
<tr class="even c35">
<td class="c33"><p><span class="c1">Broadband Modem</span></p></td>
<td class="c32"><p><span class="c1">Cellular (LTE) for
networking</span></p></td>
<td class="c29"><p><span class="c1">$300</span></p></td>
</tr>
<tr class="odd c26">
<td class="c33"><p><span class="c15">Up-facing (cloud) </span><span
class="c8"><a
href="https://www.google.com/url?q=https://hanwhavisionamerica.com/product/xnf-8010rv/&amp;sa=D&amp;source=editors&amp;ust=1693388427204976&amp;usg=AOvVaw37xaFtUp5X9nms5FNnmnCC"
class="c9">XNF-8010RV</a></span><span class="c15"> camera &amp;
down-facing (horizon) </span><span class="c8"><a
href="https://www.google.com/url?q=https://hanwhavisionamerica.com/product/xnv-8081z/&amp;sa=D&amp;source=editors&amp;ust=1693388427205183&amp;usg=AOvVaw22ZxhpJNvsI3zYxyb3ELw7"
class="c9">XNV-8081Z</a></span><span class="c1"> camera</span></p></td>
<td class="c32"><p><span class="c15">WSNs support a wide range of
standard-mount cameras.  Upgraded cameras, such as the Hanwha:
</span><span class="c15">XNV-8082R or XNV-8080 cost more, and could be
added.</span></p></td>
<td class="c29"><p><span class="c1">Included in WSN
price</span></p></td>
</tr>
<tr class="even c26">
<td class="c33"><p><span class="c1">Integrated sensing capabilities for
Wild Sage Node</span></p></td>
<td class="c32"><p><span class="c15">GPS, Rainfall Sensor (</span><span
class="c8"><a
href="https://www.google.com/url?q=https://rainsensors.com/products/rg-15&amp;sa=D&amp;source=editors&amp;ust=1693388427206203&amp;usg=AOvVaw1emLQIX8EA6d3f68jTrhV3"
class="c9">rg-15</a></span><span class="c15">), microphone,
gas,pressure, humidity and temperature sensors (</span><span
class="c8"><a
href="https://www.google.com/url?q=https://www.bosch-sensortec.com/products/environmental-sensors/gas-sensors/bme680/&amp;sa=D&amp;source=editors&amp;ust=1693388427206469&amp;usg=AOvVaw2e5yQIHiGxv8KKB1AXJlOv"
class="c9">bme 680</a></span><span class="c1">)</span></p></td>
<td class="c29"><p><span class="c1">Included in WSN
price</span></p></td>
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

<span id="t.9da740a733e479e0d93c750d5a859a1211d44a28"></span><span id="t.3"></span>

<table class="c28">
<tbody>
<tr class="odd c25">
<td class="c23"><p><span class="c22 c27 c37">Deployment size
(nodes)        </span></p></td>
<td class="c17"><p><span
class="c22 c27 c37">Cost/year/node</span></p></td>
</tr>
<tr class="even c25">
<td class="c23"><p><span class="c6">1</span></p></td>
<td class="c17"><p><span class="c6">$16.7K</span></p></td>
</tr>
<tr class="odd c41">
<td class="c23"><p><span class="c6">5</span></p></td>
<td class="c17"><p><span class="c6">$13.3K</span></p></td>
</tr>
<tr class="even c25">
<td class="c23"><p><span class="c6">10</span></p></td>
<td class="c17"><p><span class="c6">$9.8K</span></p></td>
</tr>
<tr class="odd c25">
<td class="c23"><p><span class="c6">20</span></p></td>
<td class="c17"><p><span class="c6">$8.3K</span></p></td>
</tr>
<tr class="even c25">
<td class="c23"><p><span class="c6">30</span></p></td>
<td class="c17"><p><span class="c6">$7.7K</span></p></td>
</tr>
<tr class="odd c25">
<td class="c23"><p><span class="c6">50</span></p></td>
<td class="c17"><p><span class="c6">$7K</span></p></td>
</tr>
</tbody>
</table>

<span class="c6"></span>

## Networking & Data Transfer

Networking and data transfer, for example cellular broadband LTE or
Starlink, should also be budgeted, and depends on local wireless
providers and their pricing.  WSNs not directly connected via wired
Ethernet or Starlink, will likely need an LTE modem or Wifi connection
installed during manufacturing.

## Worked Example

Given the costs above, here are some worked
examples:

**Example A**:  A single WSN with
additional Mobotix Infrared sensor connected to a Pan/Tilt
platform:

Sensors: \$10000

WSN: \$9500

Beehive Cloud Service: \$16700/yr

Broadband: \$480/yr

So the total for the first year would be: \$36,680 (equipment purchase + Beehive and broadband)

Additional years would be \$17,180 (beehive and broadband cost)

**Example B**:  A 20 node deployment: 10 WSN and 10 Sage Blades, each with an Air Quality sensor. Also, there are two Micropulse Radars (assuming \$25k each). Assume WSN nodes with LTE broadband, and Sage Blades are hard wired to the
non-metered and zero cost Internet infrastructure.

Sensors: \$3500 \* 20  +  25000 \* 2 = \$120,000

WSN: \$9500 \* 10 = \$95,000

Sage Blade: \$6500 \* 10 = \$65,000

Beehive Cloud Service: \$8300 \* 20 = \$166,000

Broadband: \$480/yr \* 10 = \$4,800

So the total for the first year would be: \$450,800 (equipment plus Beehive and broadband).

Additional years would be \$170,800 (beehive and broadband cost)

For a 3 year NSF grant, the total charged to the project for a 20 node deployment with Sage nodes and the sensors described above: \$792,400.

Not included in this worksheet of pricing:

\* Shipping of WSN nodes from local electronics
manufacturing (Chicago area)

\* Installation of nodes at destination.
