# pico-breadboard-kit
For pico breadboard kit 's 2.8 inch touch screen 


## Download and install Thonny IDE via https://thonny.org
## Install MicroPython firmware to Raspberry Pi Pico.  
	https://docs.sunfounder.com/projects/thales-kit/en/latest/micropython/python_start/install_micropython_to_pico.html
	
	### Press and hold the BOOTSEL button 
	### Connect the Pico to a computer with a Micro USB cable
	### Release the BOOTSEL button when the Pico appears as a Mass Storage Device called RPI-RP2
	### Select Install Micropython from the interpreter selection button 
	### Select Raspberry Pi.Pico/Pico H in the Micropython variant
    ### Click Install
	### Wait for the installation to finish
	
## Download or clone the geeekpi code
	### git clone https://github.com/geeekpi/picoBDK
	
## Copy the contents of the lib directory to the root of the Raspberry Pi Pico device
cd into picoBDK-main/lib
copy glcdfont.py, ili934xnew.py, tt14.py, tt24.py, tt32.py
	
## Copy the main.py from any of the three example folders.
	### i.e.  picoBDK-main/examples/button_counter/main.py
	
	
## You need to make sure that the Pin numbers are correct for your device.
	### I had to change the original code from

	    ```
		TFT_CLK_PIN = const(6)
		TFT_MOSI_PIN = const(7)
		TFT_MISO_PIN = const(4)

		TFT_CS_PIN = const(13)
		TFT_RST_PIN = const(14)
		TFT_DC_PIN = const(15)
		.
		.
		.
		addPin = Pin(17, Pin.IN) #Connect a button to pin 17
		subtractPin = Pin(16, Pin.IN) #Connect a button to pin 16

		```
	
		TO
		
		```
		TFT_CLK_PIN = const(2)
		TFT_MOSI_PIN = const(3)
		TFT_MISO_PIN = const(4)

		TFT_CS_PIN = const(5)
		TFT_RST_PIN = const(7)
		TFT_DC_PIN = const(6)
		.
		.
		.
		addPin = Pin(15, Pin.IN) #Connect a button to pin 15
		subtractPin = Pin(14, Pin.IN) #Connect a button to pin 14

		```

	### Save the file onto the Raspberry Pi Pico device
	