# subzero

Casual research in to underwater robotics powered by the Raspberry Pi Zero.

## Sensors

* Depth (Pressure)
  * [Measurement Specialties](http://www.meas-spec.com/pressure-sensors/board-level-pressure-sensors/digital-pressure-sensor-modules.aspx) has a line of amazing MEMS-based pressure sensors that are tiny, accurate, and easy to use. SparkFun has a breakout board for the [MS5803-14BA](https://www.sparkfun.com/products/12909) and [The Cave Pearl Project](https://edwardmallon.wordpress.com/2014/03/27/adding-a-ms5803-02-high-resolution-pressure-sensor/) goes in to detail on embedding external sensors in epoxy.
* Positioning
  * GPS is only really an option on the surface since water attenuates RF signals pretty quickly.
  * Many ROVs use an [underwater acoustic positioning system](https://en.wikipedia.org/wiki/Underwater_acoustic_positioning_system) such as [Long Baseline Acoustic Positioning System](https://en.wikipedia.org/wiki/Long_baseline_acoustic_positioning_system) or [Short Baseline Acoustic Positioning System](https://en.wikipedia.org/wiki/Short_baseline_acoustic_positioning_system).
  * [Inertial Navigation Systems](https://en.wikipedia.org/wiki/Inertial_navigation_system) are often used to augment other systems.
* Bottom (Depth sonar), sometiles called an Altimeter
  * [Coconut Pi](http://www.rs-online.com/designspark/electronics/blog/coconut-pi-individual-components-development-for-an-auv) and [Model_UBoatMC](https://github.com/emmesolutions/Model_UBoatMC) have used the weatherproof but not rated for underwater use [Maxbotix MB7078](http://www.maxbotix.com/Ultrasonic_Sensors/MB7072.htm) at depths of 1-3 meters.
  * [Kongsberg](http://www.km.kongsberg.com/ks/web/nokbg0240.nsf/AllWeb/188AD958095B7127C1256CFC00300A95?OpenDocument), [Valeport](http://www.valeport.co.uk/Applications/MetrologyandPositioning/MetrologyandPositioningProductDetails/ProductID/39/List/0.aspx?SortField=ProductName,ProductName) sell commercial versions but are larger than I'd like.
  * [Oceantools](http://www.oceantools.co.uk/rov/ma500d-altimeter/) and [Tritech](http://www.tritech.co.uk/product/tritech-micron-echo-sounder-ultra-compact-altimeter) have smaller models.
  * In [Development of a Small Sonar Altimeter and Constant Altitude Controller for a Miniature Autonomous Underwater Vehicle](http://scholar.lib.vt.edu/theses/available/etd-02182005-150817/unrestricted/luan_thesis.pdf), Jessica Luan describes building her own altimeter from a waterproof transducer.
  * There are several low-ish cost ($75-175) transducers for boat fish/bottom finders from Garmin and others. The challenge here would be interpreting raw data or using an NMEA 0183 or NMEA 2000 transducer and decoding that.
  * [Mark Thompson](http://www.mbtelectronics.com/side-scan-sonar.php) shares in detail his home built side-scanning sonar.
  * [The Ardupilot controlled transducer boat](http://diydrones.com/profiles/blogs/the-ardupilot-controlled-transducer-boat-part-3) details a surface-based sonar vessel powered by Ardupilot.

## Thrusters and other components

* [Bue Robotics](http://www.bluerobotics.com/) has a relatively inexpensive electrical thruster that they funded with Kickstarter. They also carry cast acrylic watertight enclosures and end-cap cable penetrators.
* Lots of DIY builds involve repurposing an electric bilge pump, removing the housing, and adding a propeller. 

## Communication

* Most ROVs use a tether to communicate. Tethers appear to be the only way to carry enough bandwidth from the ROV to base station to cover the requirements of live video and other sensor/telemetry requirements.
* I plan to experiment with [RTL SDR](http://www.rtl-sdr.com/) inexpensive software defined radios at the lower end of their useful spectrum (20-100MHz) to see if there's a way to carry a little bit of bandwidth longer distances.
* [UCSD](http://cseweb.ucsd.edu/~b1benson/publications/oceans10.pdf) have created an extremely low bandwidth (200 BPS) but long distance (2km) acoustical modem for $600. Other commercial options include LinkQuest and Teledyne Benthos in the $8k-$10k range.
* [WHOI Micromodem](http://acomms.whoi.edu/micro-modem/) is also in the $8k range.
* [Ryan Kastner at UCSD](http://kastner.ucsd.edu/ryan/underwater-communications/) talks about a custom transducer modem.
* [Northeastern University](http://www.ece.neu.edu/wineslab/underwater_sensor_networks.php) has done some research on underwater sensor networks.
* The team behind [Design and Implementation of an Omni-Directional Underwater Acoustic Micro-Modem Based on a Low-Power Micro-Controller Unit](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3304167/) from the journal Sensors looks at transmission loss at various frequencies and builds their own underwater modem with a transducer. They reach 5kbps at 30m using a 70MHz transducer.
* [Aquasent](http://www.aquasent.com/acoustic-modems/) is a commercial underwater modem provider.
* [Mike's Sub Works](http://www.mikessubworks.com/) uses 75 MHz RC gear to communicate with small ROVs.

## Other projects

* [ROVs in a Bucket](http://monitor.noaa.gov/publications/education/rov_manual.pdf) walks through an inexpsneisve ROV build with PVC pipe and modified bilge pumps as thrusters.
* [OpenROV](http://www.openrov.com/) have been working on ROVs in the open for awhile and also sell kits.
* [Cornell University Autonomous Underwater Vehicle](http://www.cuauv.org/) contains lots of information about their builds and [lots of open source software](https://github.com/cuauv/software). They [published a paper](http://www.cuauv.org/pdfs/Cornell_Journal_Paper_RS15.pdf) about their most recent vehicle, Argo.
* [ArduPilot](http://ardupilot.com/) is a long running successful project that encompasses hardware and mission planning mostly for airborne UAVs. No direct applications to AUVs but lots of things were learned the hard way here.
* [Coconut Pi](https://coconutpi.wordpress.com) a Raspberry Pi and ArduPilot project from 2013.
* [The Robot Operating System](http://www.ros.org) is used in many land-based robots and some UAVs and is worth further investigation.
* [Collective Cognitive Robots](http://cocoro.uni-graz.at/drupal/) is researching collaboration between swarms of underwater robots.
* [Amador Valley High School Robotics Club Barracuda](http://www.avbotz.com/ourauv/) for the [RoboSub competition](http://www.auvsifoundation.org/foundation/competitions/competition-central/robosub).

## Books and Articles

* [The ROV Manual, Second Edition: A User Guide for Remotely Operated Vehicles](http://www.amazon.com/dp/0080982883): This focuses on observation-class ROVs and larger, and has a lot of information a small ROV/AUV can ignore. Overall it's a good into that filled in the state of the art of sensors and other things. It goes in to a ridiculous amount of detail of some things and glosses over others, but it's a helpful bootstrap.
* [Underwater Robotics : Science, Design and Fabrication](http://www.amazon.com/dp/0984173706) is the other big book on the subject. I haven't skimmed through this one.
* [The American Practical Navigator](http://msi.nga.mil/NGAPortal/MSI.portal?_nfpb=true&_pageLabel=msi_portal_page_62&pubCode=0002), first published by Bowdich and updated by lots of people has lots of background on navigation.
* [The Internet Underwater: An IP-compatible Protocol Stack for Commercial Undersea Modems](http://www.ece.neu.edu/wineslab/papers/Yifan_WUWNet2013.pdf) a paper about running a full TCP/IP stack on the Teledyne Benthos SM-75.
* [An Evaluation of Potential Operating Systems for Autonomous Underwater Vehicles](www.dtic.mil/get-tr-doc/pdf?AD=ADA591400) [PDF] compares general and embedded operating systems as well as many robotics-oriented platforms.
* [Achieving High Navigation Accuracy Using Inertial Navigation Systems in Autonomous Underwater Vehicles](http://auvac.org/uploads/publication_pdf/Achieving-High-Navigation-Accuracy-using-INSs-in-AUVsPanishJune-2011.pdf) details the intertial navigation system of the Bluefin AUV.

## Simulation

* [UWSim](http://www.irs.uji.es/uwsim/) is an open source dedicated ROV/AUV simulator for Linux.
* [Gazebo](http://gazebosim.org) is an open source cross-platform general robotics simulator. AUV plugins include [gazebo-uav-sim](https://github.com/msporyshev/gazebo-auv-sim) and [freefloating_gazebo](https://github.com/freefloating-gazebo/freefloating_gazebo).
* [MARS](http://www.iti.uni-luebeck.de/forschung/mobile-robotik/mars.html) the MArine Robotics Simulator is designed for hardware-in-the-loop testing of AUVs, integrating with ROS and several robots developed at Institut für Technische Informatik.

## Websites

* [Woods Hole Oceanographic Institution](http://www.whoi.edu/) has [an AUV page](http://www.whoi.edu/main/auvs) with links to several vehicles.
* [The Cave Pearl Project](https://edwardmallon.wordpress.com/) has a lot of info on DIY encasing and sensors.
* [The Autonomous Undersea Systems Institude](http://ausi.org/)
* [Autonomous Undersea Vehicle Applications Center](http://auvac.org/)
* [Homebuild ROVs](http://www.homebuiltrovs.com/rovforum/index.php) forum
* [RC-Sub-Workshop](http://www.rc-sub-workshop.com) is aimed at functional RC scale models but has great prices on acrylic tubes, motors, and specialized electronics.
* [The SubCommittee](http://www.subcommittee.com) is a group of scale RC sub enthusiasts with lots of basic information and links to vendors.

## Vehicle Design

### Version 0: Sensors on a Line

The first task is to construct a platform for component validation. This will likely be a small watertight enclosure weighted for negative bouyancy suspended from the surface from a line. A minimal set of components:

* Raspberry Pi Zero
* Power source (USB battery pack?)
* Sensors
  * Pressure/temperature
  * Bottom/distance

This should also be able to serve as a communications test platform, but that's not strictly required for initial testing.
