# Capacitive MIDI Controller

This is an Arduino MIDI controller built on 8 capacitive sensing pads.

See video here: https://www.instagram.com/p/CmBSbo3A0wY/?utm_source=ig_web_button_share_sheet

Made by Iulian Radu, 2022.

## Wiring:
   - There are 8 capacitive sensors which act as midi buttons
   - Each capacitive pad is connected to a send pin and receive pin, and works like this (see image on https://playground.arduino.cc/Main/CapacitiveSensor/)
   ---- Arduino signal comes through the send pin, passes through a capacitor (1M?), and discharges through the capacitive pad and also the receive pin
   - Arduino pins 2 and 3 are the "send pins" for capacitive sensing
   - Arduino pins 8,9,10,11 are the "receive pins" for capacitive sensing connected to "send pin" 2 (you'll need resistors on each one)
   - Arduino pins 4,5,6,7 are the "receive pins" for capacitive sensing connected to "send pin" 3 (you'll need resistors on each one)
   - If your piano buttons are laid oud differently than mine (ie: you want the notes in a different order), then change the order of these capacitive sensors in the "cs" array
   - If you want completely different notes, you'll need to change the calls to sendNoteOn()

## Requires other software on your computer:
  - HairlessMIDI (for USB to MIDI conversion)
  - LoopMIDI (for MIDI device to MPC Beats / DAW)
  - DAW (ex: MPC Beats)

## This is constructed from info on these sites:
  - midi controller: https://www.instructables.com/DIY-USB-Midi-Controller-With-Arduino-a-Beginners-G/
  - capacitive sensing: https://playground.arduino.cc/Main/CapacitiveSensor/
  

