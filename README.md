# Simple-USB-MIDI-Implementation-on-STM32F103-with-CubeIDE

This is a simple project to demonstrate the USB MIDI implementation on STM32F103 device using CubeIDE and its inbuilt-libraries. Here the stm32f103c8t6 based board, also known as blue-pill is programmed such that it sends MIDI-Note-On and MIDI-Note-off messages to the host alternatively every 0.5 seconds. The code here can be upgraded to a full fledged MIDI keyboard, by adding switches/ buttons to the microcontroller to send the appropriate notes w.r.t each button press.

Youtube Video:
  

Potential drawback of this implementation:
  In this implementation we are modifying the existing Mouse HID demo code to act as MIDI device, and we are using the USBD_HID_SendReport function to send the MIDI data to the host (i.e, PC, Smartphone, MIDI Synth, etc), but the procedure to receive MIDI data from host is not implementaed here, and I am not sure how easy that would be. Since I am not an expert in USB protocols and STM32 microcontrollers, I will have to leave that part to professionals and experts.

References:
  https://www.usb.org/sites/default/files/midi10.pdf
  https://en.wikipedia.org/wiki/MIDI#:~:text=MIDI%20notes%20are%20numbered%20from,A0%20to%20C8.
  https://www.midi.org/specifications-old/item/table-1-summary-of-midi-message
  https://www.midi.org/specifications-old/item/table-2-expanded-messages-list-status-bytes
  https://github.com/essigt/SpareFaders
