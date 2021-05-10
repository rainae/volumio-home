# setup volumio 2 to run with rpi-cirrus soundcard

place the files from this repo on the target image in the following places:

* cirrus.conf -> /etc/modprobe.d/cirrus.conf

* dacs.json.cirrus-headphones or dacs.json.cirrus-spdif -> /volumio/app/plugins/system_controller/i2s_dacs/dacs.json

* Playback_to_Headset.sh
  Playback_to_Lineout.sh
  Playback_to_SPDIF.sh
  Playback_to_Speakers.sh
  rpi-cirrus-functions.sh

  -> /volumio/app/plugins/system_controller/i2s_dacs/scripts/

* in case of Headset output, inside volumio the kind of mixer needs to be Hardware, where the mixer-type needs to be "HPOUT1 Digital" and the Maximum Volume needs to be set lower then 100 (e.g. 30).

* in case of SPDIF output, inside volumio the kind of mixer needs to be Software
