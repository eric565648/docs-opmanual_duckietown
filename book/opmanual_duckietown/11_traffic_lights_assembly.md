# Traffic Lights Assembly {#traffic-light-assembly status=draft}

Assigned: Marco Erni (Eric Lu is working on it.)

This document describe how to build traffic lights in your Duckietown. Since we installed surveillant cameras on traffic lights too, we'll explain all hardware parts here and leave the software description to next chapter.

## Overview

Traffic lights are crucial parts in modern cities. We rely on them to have well-organized traffic. While antonymous cars could communicate with each other through so many different kinds of communication protocol, humans can't. Unless you are a terminator, or a RoboCop, or Neo. In the near future where autonymous cars drive with human drivers, we still need the help of traffic lights.

About the hardware part, the traffic light is composed with two wooden boxes on the diagonal direction of an intersection. On of them is equipped with raspberry pi and other cables for localization usage.

TODO: Add a photo of one intersection with a traffic light.

Traffic lights node are expected to launch whenever they turn on.

## Bill of Material

Here is the bill for assemble "one set" of traffic light.

<div markdown="1">

 <col2 id='materials-trafficlight' figure-id="tab:materials-trafficlight" figure-caption="Bill of materials for traffic light">
    <s>[Wooden Plates] </s>                         <s>USD ??</s>
    <s>[Tubes] </s>                         <s>USD ??</s>
    <s>[Rpi B+](https://tinyurl.com/ybyng4hf) </s>                         <s>USD 35</s>
    <s>[Pi Camera H](https://goo.gl/yVDp3a) </s>                         <s>USD 39</s>
    <s>[1m Camera Cable](https://www.adafruit.com/product/2143) </s>                         <s>USD 3.95</s>
    <s>[16 GB Class 10 MicroSD Card](https://tinyurl.com/ydawrgdx) </s>                         <s>USD 10</s>
    <s>[3m USB to Micro USB Cables](https://goo.gl/BHfaYY) </s>                         <s>USD 2.99</s>
    <s>[USB Charger](https://goo.gl/PNeiTb) </s>                         <s>USD 30</s>
    <s>[LED] </s>                         <s>USD 30</s>
    <s>[Jumper Wire] </s>                         <s>USD 30</s>
    <s>[Glue](https://tinyurl.com/y87xjpx8) </s>                         <s>USD 1.7</s>
    <s>Total for a set of Traffic Light </s>                         <s>USD ??</s>
 </col2>

</div>

To form a inter-network for all traffic light and camera tower, you also need a Wifi-router and several switches depends on how large your system is.

<div markdown="1">
 <col2 id='materials-inter-network' figure-id="tab:materials-inter-network" figure-caption="Bill of materials for inter-network">
    <s>[Switch](https://goo.gl/xEG6Xq) </s>                         <s>USD 76.7</s>
    <s>[Wifi-router](https://tinyurl.com/y8ej59qz) </s>                         <s>USD 460</s>
 </col2>
</div>

## Hardware Preparation

### From Wooden Plates to Chasis Parts (Laser Cut):
The plates should be 4mm thick. To cut a set of traffic light, you need a plates with the size of roughly ??x??x??.
Here's the link of laser cut file.

> [https://drive.google.com/file/d/11j4E1i60_-s6tBH37SbpPSEgYIcDF1X0/view?usp=sharing](https://drive.google.com/file/d/11j4E1i60_-s6tBH37SbpPSEgYIcDF1X0/view?usp=sharing)


TODO: Calculate how large a plates needed to cut a set of traffic light.

TODO: Give the cutting of middle part (light chasis)

### Tubes Preparation:
We need three kinds of length of tubes for a set of traffic light,

<col2 figure-id="tab:escapes" figure-caption="Symbols to escape">
    <s>Tube 1: </s> <s>572mm</s>
    <s>Tube 2: </s> <s>1120mm</s>
    <s>Tube 3: </s> <s>262mm</s>
</col2>

We recommend you to buy a tube cutter. It'll save you from lots of troubles.
You only need Tube 1 if you are only assembling camera towers.

After cutting tubes, you need to drill some holes on these tubes for wires to go through. (If you are only building this for camera towers, then you can skip this part.)
Also, we recommend you to buy a hole driller. It'll save a lot of time too, and it's fun to use this little gadget.

TODO: Add the spec of holes.

TODO: Add picture of tube cutter

TODO: Add picture of tube driller

## Hardware Assembly
For the hardware assembly, we'll start with the side with Raspberry Pi while it's the same on the other side only that you don't need to insert an Raspberry Pi.

### Wooden Box (with Rpi)
These are all the parts for assembly the wooden box.
<div figure-id="fig:boxes_part" figure-caption="The parts for wooden box assemble.">
  <img src="traffic_light/parts.jpg" style='width: 30em; height:auto'/>
</div>

##### Step 1: Stick the sliders
<div figure-id="fig:step1" figure-caption="Step 1">
  <img src="traffic_light/Step1.png" style='width: 25em; height:auto'/>
</div>

##### Step 2: Combine two walls of the box
<div figure-id="fig:step2" figure-caption="Step 2">
  <img src="traffic_light/Step2.png" style='width: 25em; height:auto'/>
</div>

##### Step 3: Stick the third wall of the box
<div figure-id="fig:step3" figure-caption="Step 3">
  <img src="traffic_light/Step3.jpg" style='width: 25em; height:auto'/>
</div>

##### Step 4: Stick the forth wall of the box
<div figure-id="fig:step4" figure-caption="Step 4">
  <img src="traffic_light/Step4.jpg" style='width: 25em; height:auto'/>
</div>

##### Step 5: Stick the stabler for the tube
Stick the small part, but DON'T stick the large plate. It should be the lid for the box that can be opened so that we could put Raspberry Pi in.
<div figure-id="fig:step5" figure-caption="Step 5">
  <img src="traffic_light/Step5.jpg" style='width: 25em; height:auto'/>
</div>

##### Step 6: Get the parts for camera mount
<div figure-id="fig:step6" figure-caption="Step 6">
  <img src="traffic_light/Step6.jpg" style='width: 25em; height:auto'/>
</div>

##### Step 7: Stick the stablers for tubes on camera mount
Note that there're two parts with larger holes and one part with a smaller hole. Tubes can go through lager hole but not smaller one. Thus, you should place the parts with smaller on the very top.
<div figure-id="fig:step7" figure-caption="Step 7">
  <img src="traffic_light/Step7.png" style='width: 25em; height:auto'/>
</div>

##### Step 8: Stick the other side of camera mount
<div figure-id="fig:step8" figure-caption="Step 8">
  <img src="traffic_light/Step8.png" style='width: 25em; height:auto'/>
</div>

##### Step 9: Stick the little T shape part on the lid of camera mount
You don't need to stick the lid on the camera.
<div figure-id="fig:step9" figure-caption="Step 9">
  <img src="traffic_light/Step9.jpg" style='width: 25em; height:auto'/>
</div>

...


TODO: Finish the rest steps

### LED Mount

TODO: Take step-picture of LED Mount

### Connector

TODO: Take step-picture of Connector

### Connect Two Wooden Box and LED Mount

TODO: Take pictures and add steps to that.

## Software Setup

### Image Prepare
Prepare a Duckiebot image and remember to add your machine file (till 11.5)

See: [](#setup-duckiebot)

and this chapter

See: [](#rc-control)

Please use "tlo" for all traffic light/camera tower username, and "trafficlight#" for hostname. (# indicate 1, 2, 3..etc.) Also we suggest you to give every traffic light a same password.

After this step, you should have a traffic light image name.

    tlo@trafficlight1.local


### Launch Traffic Lights
SSH into the traffic light, and source environment and set ROS master

    duckiebot $ cd ~/duckietown
    duckiebot $ source environment.sh
    duckiebot $ source set_ros_master.sh

After this step, launch traffic light node.

    duckiebot $ make demo-traffic-light

You should see the traffic light shining like crazy now.
