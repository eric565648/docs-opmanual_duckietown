# Auto-Localization Overview {#auto-localization-overview status=draft}

Assigned: Eric Lu, Josephine Quack

The auto-localization system is an important part of AI-DO competition. Since we need to score each team with the performances of their cars, it's necessary to have a system to localize and track the movement of these Duckiebots.

## Overview

The ultimate goal of these watch towers is to localize all Duckiebots in the town. Although we could install an overhead camera and make it act like a GPS system, we feel like running the whole Duckietown system without external machines. Thus, these watch towers are installed as if those surveillant cameras on the street and we leveraged them to localize all Duckibots.

The watchtowers and the whole auto-localization

The hardware part of the watch towers is almost the same as traffic light and even simpler. It's simply a traffic light without the wooden box on the other side and the horizontal tube.

The software part of the watch tower is much more complex. It includes the whole system of localization. We'll explain it later.

## Bill of Material



<div markdown="1">

 <col2 id='materials-watchtower' figure-id="tab:materials-watchtower" figure-caption="Bill of materials for a watchtower">
    <s>[Wooden Plates] </s>                    <s>USD ??</s>
    <s>[Tubes] </s>                         <s>USD ??</s>
    <s>[Rpi B+](https://tinyurl.com/ybyng4hf) </s>                         <s>USD 35</s>
    <s>[Rpi B+ Heat Sink]() </s>                         <s>USD 10</s>
    <s>[Pi Camera G](https://tinyurl.com/y9dnv2x5) </s>                         <s>USD 28.99</s>
    <s>[1m Camera Cable](https://www.adafruit.com/product/2143) </s>                <s>USD 3.95</s>
    <s>[16 GB Class 10 MicroSD Card](https://tinyurl.com/ydawrgdx) </s>              <s>USD 10</s>
    <s>[3m USB to Micro USB Cables](https://goo.gl/BHfaYY) </s>                <s>USD 2.99</s>
    <s>[5m thin Ethernet cables]() </s>                <s>USD 7.99</s>
    <s>[USB Charger] </s>                         <s>USD 30</s>
    <s>[Glue](https://tinyurl.com/y87xjpx8) </s>                         <s>USD 1.7</s>
    <s>[M2.5, 12mm Spacers * 2]() </s>                         <s>USD 1</s>
    <s>[M2.5, 6mm Screws * 2]() </s>                         <s>USD 1</s>
    <s>[M2.5, 4mm Screws * 2]() </s>                         <s>USD 1</s>
    <s>Total for a set of watchtower</s>                         <s>USD ??</s>
 </col2>

</div>

## Hardware

See hardware part in chapter [](#traffic-light-assembly)

## Software Setup

TODO: Document them after development

### Image Prepare

#### Prepare one Duckibots Image

Prepare this Image until Step 8.11 but DON’T do ssh configuration. (You could do Step 8.14 if you wants Duckie Logos)

Name the watchtower `mom@watchtower01` with username `mom` and hostname `watchtower01`. Set the password to `MomWatches`.

See: [](#setup-duckiebot)

If you wanna skip step 1~4 and save some time, you could simply download this image.

> [https://www.dropbox.com/s/8utdpl5lgi2pumo/duckiebot-RPI3-AD-2017-09-12.img.xz?dl=1](https://www.dropbox.com/s/8utdpl5lgi2pumo/duckiebot-RPI3-AD-2017-09-12.img.xz?dl=1)

We have prepare the image above for you. It has username `mom`, hostname `watchtower01` and password `MomWatches`. Also, it already upgrade to the version for Raspberry Pi B+.

Please note that in this image, since we will connect watchtowers to the network through ethernet cables, we deleted the Duckietown Wifi network file and it won't connect to duckietown network automatically so that it won't interfere the Ethernet network.

#### Prepare other 49 Images

There're two option for copying to 49 SD cards.

##### Option 1: Use SD card Duplicator

Buy a SD Card Duplicator, plug in source SD Card and target SD cards, click the start button, then you are done!

Although it's a pretty fast and convenient way, we found that a cheap duplicator could miss copying some library or system file due to its method of copying. Thus we recommend you buy a duplicator that do copy "bit by bit" (raw data copying) or choose option 2.

##### Option 2: Burn image to multiple SD cards at once

Save your first image from SD cards to laptop.
First plug in the SD card and umount it, you can see this chapter as reference.

See: []()

Then use this command to save image from the SD card.

    $ sudo dd bs=4M if=/dev/ of=~/watchtower.img status=progress

After this step, you will have your watchtower image in your laptop.

Then, put SD cards into USB adapters, insert as many USBs-SD cards as you can to your laptop. Burn the watchtower image to those image simultaneously.

See: []()


#### Change Configuration of each watchtower image

At this point you are almost done. Insert one SD card into Raspberry Pi, connect it with ethernet cable and do ssh.

    $ ssh mom@watchtower01.local

You are now inside the watchtower, now we're setting up customize configuration for each watchtower.

First, checkout 8.11 SSH configuration and set up the ssh configuration. You only need to do basic SSH config, create key pair.

See: []()

Afterwards, change the hostname of the watchtower into `wathctowerXX`, where XX means the number for the wathctower.

That's all! Redo the step for each SD card then you'll have all the SD cards ready.

### Camera Calibration
