This is a Python library for decoding the Victron Energy VE.Direct text protocol used in their range of MPPT solar charge controllers.

This work is heavily based on the [https://github.com/karioja/vedirect] (VEDirect) package. 

The VEDirect package directly reads the stream from the serial port. It is modified to read data from a (Telnet) server which in turn may get them from a Victron device. Available on the command line it provides scripting options in a termux environment running on a smartphone. Termux must not access the serial port of the host environment system by design. However there is an Android app reading serial streams received via an OTG cable and providing it to clients using Telnet.

The only Victron device I have is the smart solar controller MPPT 75/15. Its serial port is connected to the phone via a [https://www.bjoerns-techblog.de/2021/10/victron-smartsolar-laderegler-auslesen-grundlagen] (self-made USB UART connector) and an OTG cable.

This library was tested on my old 'Huaweii P9 light' with 'Termux' from 'Fdroid' and the [https://play.google.com/store/search?q=usb%20serial%20telnet%20server&c=apps] (USB Serial Terminal Server) installed. In Termux 'python3' with 'pip3' is availanble. Unfortunately the phone cannot be charged with a regular OTG cables connected.

To install:
* Clone the project
* Enter the directory 'vesocket'
* pip install .

To test
* Enter the directory 'examples'
* Plug the OTG cable into the phone
  -> Serial USB stream app is started automtically
* ./victron_print.py
  -> Dump output to the screen

The script 'victron_mqtt.py' is only ported but not tested yet.
