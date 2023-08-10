# README #

_**Ukufika**_ is a Raspberry Pi based IOT application that displays the bus arrival time and other information for the given bus stops in Singapore. It uses [Data Mall API](https://datamall.lta.gov.sg/content/datamall/en.html) from [Land Transport Authority (LTA), Singapore](https://www.lta.gov.sg/content/ltagov/en.html).

## Components ##

* [Raspberry Pi Zero W](https://www.raspberrypi.com/products/raspberry-pi-zero/) (any version is supported)
* [Waveshare 4.2inch e-Paper Display](https://www.waveshare.com/wiki/4.2inch_e-Paper_Module)

## Technology ##

_**Ukufika**_ has been developed and tested in [Python 3.9.2](https://www.python.org/downloads/release/python-392/). However, any Python 3x version is supported. 

## Setup ##

Follow the below table to connect the EPD display with the Raspberry Pi:

| **e-Paper** | **Raspberry Pi (BCM2835)** | **Raspberry Pi (Board)** |
|:-----------:|:--------------------------:|:------------------------:|
|   **VCC**   |            3.3V            |           3.3V           |
|   **GND**   |            GND             |           GND            |
|   **DIN**   |            MOSI            |            19            |
|   **CLK**   |            SCLK            |            23            |
|   **CS**    |            CE0             |            24            |
|   **DC**    |             25             |            22            |
|   **RST**   |             17             |            11            |
|  **BUSY**   |             24             |            18            |


## Installation ##

* Check for the [latest version](https://github.com/ujjaldey/Ukufika/releases/latest) of _**Ukufika**_.
* Grab the link for the repository content in `tar.gz` format.
* Login to Raspberry Pi console using PuTTY. Please make sure you are connected to internet.
* Execute the `wget` command to download the file. Example: `wget https://github.com/ujjaldey/Ukufika/archive/refs/tags/0.0.tar.gz`.
* Extract the content: `tar -xvf 0.0.tar.gz`. It will create a directory with the name `Ukufika-0.0`.
* Change directory: `cd Ukufika-0.0`.
* Execute the script: `./installer.run`.
* Follow the on-screen instructions to install _**Ukufika**_.
* Ensure to update `.env` file with the API token and `data/bus_data.json` file with the bus stop and bus service number configuration. 
* Once the installation is completed, restart the Raspberry Pi. If you have enabled the start-up on boot, Ukufika will be started automatically.

## Support ##

Please check the [project page](https://ujjaldey.in/projects/ukufika/) for more detailed instructions.

I would like to hear from you. If you have any issues or suggestions, please feel free to contact me at [ujjaldey@gmail.com](mailto:ujjaldey@gmail.com).

Thanks for using _**Ukufika**_.