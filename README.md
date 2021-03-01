# ultrasonic-garage-park-assist
Use a HC-SR04 Ultrasonic Sensor to help know when to stop the car when pulling into the garage. I'm using a NodeMCU, but this should work with any ESP8266 type board. I'm also using ESPHome on the 8266 Controller and Home Assistant.

My goal was to make it easy for the wife to pull in the garage and know when to stop so the back of her car would clear the garage door. I used to use a short 2x4 laying on the floor, but it would end up being kicked around and end up in the wrong location. I thought about the tennis ball on a string, but who wants to keep ducking around a tennis ball when walking around their garage.

The Sensor is mounted under a shelf at the far-end wall (from the large garage door). 
There are 3 "zones" set up. You can see these in the parking_assist.yaml file in the on_value: section. You'll want to change those numbers to suit your situation.
  1. under 2.4 meters
  2. under 1.6 meters
  3. under .8 meter

There are 3 indicators that will show up in the Home Assistant Dashboard. You could have these NOT visible in the dashboard simply hiding them in the dashboard. I am using these scripts to flash the overhead ceiling light so the wife knows when to stop pulling in and park her car. This is set up in a script in Home Assistant
  1. Parking Slowflash
  2. Parking Fastflash
  3. Parking Stop

With Home Assistant, I set a script for the different two different speeds flasing the overhead light, and an automation so this device is only active when the door is open.

More info to follow.
