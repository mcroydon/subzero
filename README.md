# subzero

Casual research in to underwater robotics powered by the Raspberry Pi Zero

## Sensors

* Depth (Pressure)
  * [Measurement Specialties](http://www.meas-spec.com/pressure-sensors/board-level-pressure-sensors/digital-pressure-sensor-modules.aspx) has a line of amazing MEMS-based pressure sensors that are tiny, accurate, and easy to use. SparkFun has a breakout board for the [MS5803-14BA](https://www.sparkfun.com/products/12909) and [The Cave Pearl Project](https://edwardmallon.wordpress.com/2014/03/27/adding-a-ms5803-02-high-resolution-pressure-sensor/) goes in to detail on embedding external sensors in epoxy.
* Positioning
  * GPS is only really an option on the surface since water attenuates RF signals pretty quickly.
  * Many ROVs use an [underwater acoustic positioning system](https://en.wikipedia.org/wiki/Underwater_acoustic_positioning_system) such as [Long Baseline Acoustic Positioning System](https://en.wikipedia.org/wiki/Long_baseline_acoustic_positioning_system) or [Short Baseline Acoustic Positioning System](https://en.wikipedia.org/wiki/Short_baseline_acoustic_positioning_system).
  * [Inertial Navigation Systems](https://en.wikipedia.org/wiki/Inertial_navigation_system) are often used to augment other systems.

## Thrusters

* [Bue Robotics](http://www.bluerobotics.com/) has a relatively inexpensive electrical thruster that they funded with Kickstarter.
* Lots of DIY builds involve repurposing an electric bilge pump, removing the housing, and adding a propeller. 

## Communication

* Most ROVs use a tether to communicate. Tethers appear to be the only way to carry enough bandwidth from the ROV to base station to cover the requirements of live video and other sensor/telemetry requirements.
* I plan to experiment with [RTL SDR](http://www.rtl-sdr.com/) inexpensive software defined radios at the lower end of their useful spectrum (20-100MHz) to see if there's a way to carry a little bit of bandwidth longer distances.
* [UCSD](http://cseweb.ucsd.edu/~b1benson/publications/oceans10.pdf) have created an extremely low bandwidth (200 BPS) but long distance (2km) acoustical modem for $600. Other commercial options include LinkQuest and Teledyne Benthos in the $8k-$10k range.
* [WHOI Micromodem](http://acomms.whoi.edu/micro-modem/) is also in the $8k range.
* [Ryan Kastner at UCSD](http://kastner.ucsd.edu/ryan/underwater-communications/) talks about a custom transducer modem.
* [Northeastern University](http://www.ece.neu.edu/wineslab/underwater_sensor_networks.php) has done some research on underwater sensor networks.
* [Aquasent](http://www.aquasent.com/acoustic-modems/) is a commercial underwater modem provider.
* [Mike's Sub Works](http://www.mikessubworks.com/) uses 75 MHz RC gear to communicate with small ROVs.

## Other projects

* [ROVs in a Bucket](http://monitor.noaa.gov/publications/education/rov_manual.pdf) walks through an inexpsneisve ROV build with PVC pipe and modified bilge pumps as thrusters.
* [OpenROV](http://www.openrov.com/) have been working on ROVs in the open for awhile and also sell kits.
* [Cornell University Autonomous Underwater Vehicle](http://www.cuauv.org/) contains lots of information about their builds and [lots of open source software](https://github.com/cuauv/software). They [published a paper](http://www.cuauv.org/pdfs/Cornell_Journal_Paper_RS15.pdf) about their most recent vehicle, Argo.
* [ArduPilot](http://ardupilot.com/) is a long running successful project that encompasses hardware and mission planning mostly for airborne UAVs. No direct applications to AUVs but lots of things were learned the hard way here.

## Books and Articles

* [The ROV Manual, Second Edition: A User Guide for Remotely Operated Vehicles](http://www.amazon.com/dp/0080982883): This focuses on observation-class ROVs and larger, and has a lot of information a small ROV/AUV can ignore. Overall it's a good into that filled in the state of the art of sensors and other things. It goes in to a ridiculous amount of detail of some things and glosses over others, but it's a helpful bootstrap.
* [Underwater Robotics : Science, Design and Fabrication](http://www.amazon.com/dp/0984173706) is the other big book on the subject. I haven't skimmed through this one.
* [The American Practical Navigator](http://msi.nga.mil/NGAPortal/MSI.portal?_nfpb=true&_pageLabel=msi_portal_page_62&pubCode=0002), first published by Bowdich and updated by lots of people has lots of background on navigation.

## Websites

* [Woods Hole Oceanographic Institution](http://www.whoi.edu/) has [an AUV page](http://www.whoi.edu/main/auvs) with links to several vehicles.
* [The Cave Pearl Project](https://edwardmallon.wordpress.com/) has a lot of info on DIY encasing and sensors.
* [The Autonomous Undersea Systems Institude](http://ausi.org/)
* [Autonomous Undersea Vehicle Applications Center](http://auvac.org/)
* [Homebuild ROVs](http://www.homebuiltrovs.com/rovforum/index.php) forum
