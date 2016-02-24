##Attiny2313-USB-MIDI

Modified version of the "USB-MIDI Converter もこ" project by <https://twitter.com/morecat_lab>. 

Original project details can be found from: <http://morecatlab.akiba.coocan.jp/morecat_lab/MOCO-e.html>

###Modifications
	
* Opitimised MIDI decoding algorithm. Original firmware were missing notes when played in chord shapes and somewhat fast manner. I wrote a simpler, interrupt based MIDI decoder. My version of the decoder only designed to work with *Note On* and *Note Off* events. Decoder also supports running status.

* Modified firmware automatically discards Midi Beat Clock (0xF8) and Active Sense (0xFE) commands coming from the slave device to speed up the decoding process.
	
* Made the firmware compatible with the avr-gcc 4.8.1 by changing *PROGMEM* variables to *const PROGMEM* variables.

###Build Photo

![](./img/build.jpg)

