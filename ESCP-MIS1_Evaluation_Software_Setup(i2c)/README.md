<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><blockquote>
<p>ESCP-BMS1 Evaluation Software Manual</p>
</blockquote></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>Title</p>
</blockquote></td>
<td><blockquote>
<p>ESCP-MIS1 Evaluation Software Manual</p>
</blockquote></td>
</tr>
<tr class="even">
<td><blockquote>
<p>Doc Ref</p>
</blockquote></td>
<td>ESS-242/091219/EXC-REV.04</td>
</tr>
</tbody>
</table>

<img src="./media/image1.png" style="width:4.024in;height:2.81874in" />

**  
**

**DOCUMENT TRACKING TABLE**

<table>
<colgroup>
<col style="width: 17%" />
<col style="width: 17%" />
<col style="width: 46%" />
<col style="width: 19%" />
</colgroup>
<thead>
<tr class="header">
<th><blockquote>
<p><strong>Version</strong></p>
</blockquote></th>
<th><blockquote>
<p><strong>Date</strong></p>
</blockquote></th>
<th><blockquote>
<p><strong>Reason or change</strong></p>
</blockquote></th>
<th><blockquote>
<p><strong>Author</strong></p>
</blockquote></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>1</p>
</blockquote></td>
<td><blockquote>
<p>12/9/2019</p>
</blockquote></td>
<td><blockquote>
<p>Initial version</p>
</blockquote></td>
<td><blockquote>
<p>N.Valantassis</p>
</blockquote></td>
</tr>
<tr class="even">
<td><blockquote>
<p>2</p>
</blockquote></td>
<td><blockquote>
<p>15/11/2022</p>
</blockquote></td>
<td><blockquote>
<p>Cosmetic &amp; installation instructions corrected</p>
</blockquote></td>
<td><blockquote>
<p>C.Papazachariou</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><blockquote>
<p>4</p>
</blockquote></td>
<td><blockquote>
<p>16/3/2023</p>
</blockquote></td>
<td><blockquote>
<p>Timestamp feature documented.</p>
<p>Table of Contents and figures added.</p>
</blockquote></td>
<td><blockquote>
<p>C.Papazachariou</p>
</blockquote></td>
</tr>
</tbody>
</table>

**  
**

# **Contents**

[1. Data Readout GUI [4](#data-readout-gui)](#data-readout-gui)

[1.1 Software Installation
[4](#software-installation)](#software-installation)

[1.2 Application Description
[4](#application-description)](#application-description)

**Table of Figures**

[Figure 1: UI description [4](#_Toc129881471)](#_Toc129881471)

[Figure 2: Plots [7](#_Toc129881472)](#_Toc129881472)

[Figure 3: Measurement File [8](#_Toc129881473)](#_Toc129881473)

[Figure 4: Timestamps [8](#_Toc129881474)](#_Toc129881474)

**  
**

# Data Readout GUI

## Software Installation

To install the Pressure Sensor Evaluation Software:

- Run setup.exe (as administrator if possible) and follow the
  installation wizard.

- Once the installation is complete run
  ESCP-MIS1_Evaluation_Software.exe

## Application Description

<img src="./media/image2.png"
style="width:6.72917in;height:5.70833in" />

<span id="_Toc129881471" class="anchor"></span>Figure 1: UI description

| **\#** | **Description**             |
|--------|-----------------------------|
| 1      | Connection row              |
| 2      | Device scan                 |
| 3      | Data display                |
| 4      | Open data graph window      |
| 5      | Log file configuration      |
| 6      | Evaluation Software version |
| 7      | Log Timestamp               |

1\. Connection Row

Use the *Serial Port* dropdown box to select the COM port that
corresponds to the Evaluation Kit and press the *Connect* button, which
upon successful connection will change color and its text will now
display *Disconnect*. Pressing *Disconnect* will stop communication with
the Evaluation Kit. After connection with the kit is established, the
software will automatically scan for connected devices (see Device Scan
below). This can take a few seconds.

2\. Device Scan

The software scans for connected devices and displays the results in a
table. The table columns indicate the channel number, an LED that goes
green when a device is connected to the channel, the device’s serial
number and the device’s I2C slave address (in hex). Device scan is
performed automatically after successfully establishing a connection
with the Evaluation Kit or can be manually started by pressing the *Scan
Devices* button. The scan progress is indicated by a progress bar below
the button. If a device is found on any channel the *Devices Connected*
LED lights green.

3\. Data display

The received data values are displayed in this table, both the
floating-point value for each measured quantity and the raw 16-bit
hexadecimal value. The user can choose which device’s data is displayed
by selecting the appropriate channel. The user can also choose the
sample rate of the data. The minimum sample rate is 1ms. The same sample
rate applies to the graphs and the *Log File*. The user can pause data
acquisition at any time by pressing the *Stop Data Acquisition* button.

4\. Open data graph window

Pressing the button will open the *Graph Window*

<img src="./media/image3.png"
style="width:6.84097in;height:6.09861in" />

<span id="_Toc129881472" class="anchor"></span>Figure 2: Plots

Using the drop-down menu (1) the user can select the quantity to
display. By default, data for all connected sensors is displayed but the
user can select/deselect any of them (2). The user can also zoom/pan the
graph area using the respective buttons (3) and clear the graph area by
pressing the *Clear History* button (4).

5\. Log File Configuration

Optionally the user can log the received data to a file. Use the
*Browse* button (folder icon) to select a directory and name for the log
file and press the button to start logging. Pressing the button again
will stop logging. Data is logged to the file at the rate specified in
the Sample Rate textbox as tab delimited values. Measured quantities are
written in the following order

| **Pressure** | **Temperature** |
|--------------|-----------------|

For each measured quantity we log its floating-point value with 7 digits
of precision. An example is shown below:

<img src="./media/image4.png" style="width:2.14613in;height:0.91679in"
alt="Text Description automatically generated" />

<span id="_Toc129881473" class="anchor"></span>Figure 3: Measurement
File

A log file for each serial number will be created storing the
corresponding data.

6\. Evaluation Software Version

Displays the current version of the application

7\. Log Timestamp

This enables the saving of timestamp data in the data measurement file
with the following format:

*Year-month-date_hour-minute-second.millisecond*

<img src="./media/image5.png"
style="width:4.85417in;height:2.57292in" />

<span id="_Toc129881474" class="anchor"></span>Figure 4: Timestamps
