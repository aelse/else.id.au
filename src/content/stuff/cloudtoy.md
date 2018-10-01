---
title: "Cloud Toy"
date: 2018-10-01T10:51:20+10:00
subtitle: "The sad cloud of IoT"
tags: [arduino]
---
I was in a shop recently and came across a child's nightlight I liked the look of. I thought it'd make the start of a good IoT project (because cloud).

![](/img/cloudtoy/cloud_nightlight.jpg)

My plan is to turn this into an indicator when things are broken. The theme will be along the lines of:

![](/img/cloudtoy/the_cloud.jpg)


## How

Using a Wemos D1 mini I can have "the cloud" connect over wifi to a message queue to receive control messages instructing it on how to configure its lights.

A separate component running elsewhere (eg. on a Raspberry Pi) will publish to the message queue in response to something happening that should cause a light change.

## Build

I put together a simple shield for a Wemos D1 mini clone. It's a proto board with a few LEDs, transistors and a resistor.

{{< gallery caption-effect="fade" >}}
  {{< figure thumb="-small" link="/img/cloudtoy/shield.jpg" caption="Shield mounted on Wemos D1 mini clone">}}
  {{< figure thumb="-small" link="/img/cloudtoy/shield_top.jpg" caption="Shield top" >}}
  {{< figure thumb="-small" link="/img/cloudtoy/shield_bottom.jpg" caption="Shield bottom">}}
{{< /gallery >}}

The result is something I can control remotely over the network via MQTT.

{{< gallery caption-effect="fade" >}}
  {{< figure link="/img/cloudtoy/board_leds.gif" caption="Blinkenlights">}}
  {{< figure link="/img/cloudtoy/cloud_leds.gif" caption="Blinkencloud" >}}
{{< /gallery >}}

The lights can be independently configured to be on or off.

## Links

* [Project on GitHub](https://github.com/aelse/cloudtoy)