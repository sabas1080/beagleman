Alexa with Raspberry Pi
Fork of BeagleMan
=======

by Andres Sabas
The Inventor's House Hackerspace
26 april 2016

###Material
- Raspberry Pi B
- USB Microphone Meteor

##Instruction
###Install dependencies


apt-get install build-essential python-dev libcurl4-openssl-dev python-pip libssl-dev wig python-alsaaudio sox espeak libsox-fmt-mp3

pip install pycurl cherrypy

change the next line in /lib/modprobe.d/aliases.conf

sudo nano /lib/modprobe.d/aliases.conf

```bash
# This sets the index value of the cards but doesn't reorder.
options snd_usb_audio index=0
options snd_bcm2835 index=1

# Does the reordering.
options snd slots=snd-usb-audio,snd-bcm2835
```

apt-get install libtool automake bison libffi-dev

Based in [BeagleMan](https://github.com/fcooper/beagleman) work
