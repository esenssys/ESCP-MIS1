# ESEK-5C-SPI Evaluation Software Manual

Doc Ref: ESS-324/220822/EXC-REV.01

**DOCUMENT TRACKING TABLE**

| **Version** | **Date** | **Reason for change** | **Author** |
| --- | --- | --- | --- |
| 1 | 5/8/2022 | Initial version | C. Papazachariou |

# **Table of Contents**

[1.Prerequisites and Installation](#c1)

[2.Application Description and operation](#c2)

# **Table of Figures**

[Figure 1: Software GUI](#f1)

[Figure 2: Connect - Disconnect button](#f2)

[Figure 3: Scan Devices](#f3)

[Figure 4: Sample rate and switch](#f4)

[Figure 5: Sampled data values](#f5)

[Figure 6: Plot quantity selection](#f5)

[Figure 7: Plots and plot options](#f6)

[Figure 8: Log button and log file path](#f8)

[Figure 9: Logged Data example](#f9)


<a name="c1"></a>
## 1. Prerequisites and Installation

- This application requires NI LabVIEW runtime 2020 32bit to run. It can be downloaded for free from NI website.

As of writing this document the runtime can be downloaded from the following link:

[https://www.ni.com/en-us/support/downloads/software-products/download.labview-runtime.html#460220](https://www.ni.com/en-us/support/downloads/software-products/download.labview-runtime.html%23460220)

- The application itself does not require installation. In order to run, simply navigate to the downloaded folder that contains the executable named "ESEK-5C-SPI.exe" and run it.

<a name="c2"></a>
## 2. Application Description and operation
A general overview of the application graphical interface can be seen in the following picture.

![f1](https://user-images.githubusercontent.com/110021229/187670732-1ce08292-d784-457d-9143-67dadd918871.png)

<a name="f1"></a>
**Figure 1: Software GUI**
<hr/>


To start using the software, first select the appropriate COM port, then click the "Connect" button which will change to "Disconnect" once the connection is established. Clicking it again will disconnect the device.

![f2](https://user-images.githubusercontent.com/110021229/187670741-56c783ae-17f6-43fc-a459-51123d78130f.png)

<a name="f2"></a>
**Figure 2: Connect - Disconnect button**
<hr/>


Below the connection port and button, there is a list of connected sensors and an indicator that the Devkit is connected. To populate this list, press the "Scan Devices" button and all appropriately connected sensors will be displayed in the list. The list describes the port of the Evaluation Kit where each sensor is connected, a status indicator led, the sensor Serial Number, and the current firmware version.

![f3](https://user-images.githubusercontent.com/110021229/187670747-2735c019-c25b-4b9a-88c9-f2f673fe8407.png)

<a name="f3"></a>
**Figure 3: Scan Devices**
<hr/>


To begin sampling the sensors, first setup the appropriate sample rate which is 500 ms by default, then click on the "Sampling" toggle switch.

![f4](https://user-images.githubusercontent.com/110021229/187670753-dc8d2890-93e0-45fe-b46d-6e8f02a66709.png)

<a name="f4"></a>
**Figure 4: Sample rate and switch**
<hr/>


The sampled pressure and temperature data per sensor, are displayed in an array format and the user can select one of the two quantities to plot as a graph

![f5](https://user-images.githubusercontent.com/110021229/187670759-b6ea506f-c57f-4d59-98b2-daf647df9287.png)

<a name="f5"></a>
**Figure 5: Sampled data values**
<hr/>


The quantity selected will be displayed as a plot in the big plot area next to the controls. The plot Legend sub-menu allows for sensor display enabling selection, color selection for each plot line displayed, as well as a Graph depth control for selecting how much time should be displayed in the graph window.

![f6](https://user-images.githubusercontent.com/110021229/187670765-75566115-d73a-4632-a9e0-25d465de4e49.png)

<a name="f6"></a>
**Figure 6: Plot quantity selection**
<hr/>


![f7](https://user-images.githubusercontent.com/110021229/187670854-02b4f2c0-d54b-4136-87a4-51573f6e47ef.png)

<a name="f7"></a>
**Figure 7: Plots and plot options.**
<hr/>


Optionally the user can log the received data to a file. Use the _Browse_ button (folder icon) to select a directory for the log files and press the button to start logging.

![f8](https://user-images.githubusercontent.com/110021229/187670860-29ca0f2a-8f5b-4c70-8483-7b29ea68dcd2.png)

<a name="f8"></a>
**Figure 8: Log button and log file path**
<hr/>



A log file for each sampling session is created with an auto-numbered file name. Pressing the button again will stop logging. By default, existing files are overwritten unless the _Append_ option is checked. Data is logged to the file at the rate specified in the Sample Rate textbox as tab delimited values. The file has 10 columns which represent sequentially the pressure and temperature readings of each sensor in the order they have been connected, as shown in the following example.

| Pressure #1 | Temperature #1 | Pressure #2 | Temperature #2 | Pressure #3 | Temperature #3 | Pressure #4 | Temperature #4 | Pressure #5 | Temperature #5 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 0 | 1.02863 | 23.883484 | 1.486506 | 23.935537 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.02863 | 23.881256 | 1.521374 | 23.931942 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.159739 | 23.883709 | 1.504195 | 23.934933 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.159739 | 23.883709 | 1.460245 | 23.936039 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.117866 | 23.876823 | 1.479252 | 23.935238 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.11659 | 23.883709 | 1.491029 | 23.945698 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.136992 | 23.884588 | 1.507447 | 23.939112 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.136992 | 23.884588 | 1.525152 | 23.938387 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.158864 | 23.888432 | 1.524794 | 23.940836 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.17171 | 23.884588 | 1.527845 | 23.943447 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1.163408 | 23.874819 | 1.524309 | 23.944149 | 0 | 0 | 0 | 0 |

<a name="f9"></a>
**Figure 9: Logged Data example**
<hr/>
