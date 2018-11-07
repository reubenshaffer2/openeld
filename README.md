# openeld
A fully open Electronic Logging Device (ELD) for drivers of Commercial Motor Vehicles (CMVs) in the USA.

In December 2017, the USDOT/FMCSA mandated the use of ELDs by drivers of CMVs in the United States.
The basic requirements and specifications are published in the FMCSR and available online but I am
unable to locate a link to the details at this moment.  I will add any links I do find to the end of
this README.  The main reason for my interest in creating a free implementation is that, in my opinion,
a free and open implementation should be available for drivers that are now required to use these
devices, rather than a few corporate entities having the ability to control the market for something
that recent laws have required the use of.  In addition, having been a software developer and user of
free software for decades now, I have found that well designed and implemented, secure software is
almost always free and community developed rather than by a corporate entity.  In short, it seems only
fair that when a citizen is required to have something that it should be available at little or no
cost and that the general public should have the opportunity to verify that their data is secure.

This is not a project that I intend to fully implement on my own.  There are parts of this project
that, while I would be able to produce a working prototype, someone more skilled in hardware design
would certainly be able to design a much more cost-effective solution.

There are at least two parts to this project:

The regulations require that hardware must be attached to the vehicle that monitors a few specific
things.  If my memory is correct, ignition status, vehicle speed, and odometer mileage is required,
but there may be a few other things as well.  The CMVs use a CAN network which can easily be connected
to using a service port.  The preferred method of connecting would be an inline connection to the
service port which would still allow another device to be connected without unplugging, and which either
housed a transceiver (bluetooth perhaps) or connected to a small transceiver box using a wire.  This
device would likely need to contain some amount of EEPROM for a queue of events to be stored awaiting
transfer to a mobile phone or tablet containing the actual ELD software.  It is my desire that schematic
diagrams, and possibly assembly instructions, be published and protected under a license such as the GNU
GPL.

The actual ELD software would be designed to run on a mobile phone and/or tablet.  I have experience
programming apps for Android devices, but have never written anything for Apple devices, which I believe
use iOS, and have never looked to see if there is an SDK for them as I have no Apple devices with which
to perform basic testing.  The details of how the ELD software is required to function are actually pretty
well documented within the FMCSRs.  It is my desire that this software be released under a license such as
the GNU GPL as well.

Any communication protocols created and used may need to be licensed differently, as it should be possible
to use them in the creation of products that the creator should be free to distribute under whatever license
they wish, and GNU GPL may be too restrictive to allow this.

JJ Keller publishes a handbook, which is available at any truck stop, which should contain all of the
relevant details regarding implementation of ELDs.  It's a small green and white book that should not
cost more than 10 USD.  It also contains all of the details about the Hours of Service (HOS) regulations
that need to be understood in order to implement the ELD.

I am fairly new to github, but I am assuming that it should be possible to grant privileges to this
repository to others.  If you are interested in becoming a contributor, send me a message.
