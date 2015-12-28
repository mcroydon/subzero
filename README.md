# subzero

Casual research in to underwater robotics powered by the Raspberry Pi Zero

## Sensors

* Depth (Pressure)
  * [Measurement Specialties](http://www.meas-spec.com/pressure-sensors/board-level-pressure-sensors/digital-pressure-sensor-modules.aspx) has a line of amazing MEMS-based pressure sensors that are tiny, accurate, and easy to use. SparkFun has a breakout board for the [MS5803-14BA](https://www.sparkfun.com/products/12909) and [The Cave Pearl Project](https://edwardmallon.wordpress.com/2014/03/27/adding-a-ms5803-02-high-resolution-pressure-sensor/) goes in to detail on embedding external sensors in epoxy.
* Positioning
  * GPS is only really an option on the surface since water attenuates RF signals pretty quickly.
  * Many ROVs use an [underwater acoustic positioning system](https://en.wikipedia.org/wiki/Underwater_acoustic_positioning_system) such as [Long Baseline Acoustic Positioning System](https://en.wikipedia.org/wiki/Long_baseline_acoustic_positioning_system) or [Short Baseline Acoustic Positioning System](https://en.wikipedia.org/wiki/Short_baseline_acoustic_positioning_system).
  * [Inertial Navigation Systems](https://en.wikipedia.org/wiki/Inertial_navigation_system) are often used to augment other systems.

## Books and Articles

* [The ROV Manual, Second Edition: A User Guide for Remotely Operated Vehicles](http://www.amazon.com/dp/0080982883): This focuses on observation-class ROVs and larger, and has a lot of information a small ROV/AUV can ignore. Overall it's a good into that filled in the state of the art of sensors and other things. It goes in to a ridiculous amount of detail of some things and glosses over others, but it's a helpful bootstrap.
* [The American Practical Navigator](http://msi.nga.mil/NGAPortal/MSI.portal?_nfpb=true&_pageLabel=msi_portal_page_62&pubCode=0002), first published by Bowdich and updated by lots of people has lots of background on navigation.

## Websites

* [Cornell University Autonomous Underwater Vehicle](http://www.cuauv.org/) contains lots of information about their builds and [lots of open source software](https://github.com/cuauv/software). They [published a paper](http://www.cuauv.org/pdfs/Cornell_Journal_Paper_RS15.pdf) about their most recent vehicle, Argo.
* [The Cave Pearl Project](https://edwardmallon.wordpress.com/) has a lot of info on DIY encasing and sensors.
* [The Autonomous Undersea Systems Institude](http://ausi.org/)
