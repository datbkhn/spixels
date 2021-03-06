SPI Pixels - Control 16 LED strips at once
==========================================
http://spixels.org/

Parallely feeding 16 SPI LED strips with a Raspberry Pi.

This is the hardware and library separated out of the [FlaschenTaschen] project
to be used independently.

This provides a Raspberry Pi Adapter to connect up to 16 SPI-type LED strips
(such as **APA102**, **WS2801**, **LPD6803**), that are fed by the Raspberry Pi
in parallel for fast update rates.

The C++ library can be found in [include/](./include) and
[lib/](./lib), with examples in the, you guessed it,
[examples/](./examples) directory.

If you want to use the library in your own projects, just add it as a
sub-module to your project:

```
git submodule add https://github.com/hzeller/spixels
```

You now have a subdirectory `spixels/` in your project. See
the [Makefile](./examples/Makefile) in the examples/ directory as a
template how to use it with your project.

You find the board in the [hardware/](./hardware) directory (including OshPark
link).

The adpater is compatible with any Raspberry Pi with 40 GPIO pins, such as the
Pi 1 B+, Pi 2 or Pi 3.

Of course, you can use the MultiSPI feature to send data to other simple
devices.
<a href="hardware/"><img src="img/pi-adapter-pcb.png" width="400px"></a>
<a href="img/pi-adapter-irl.jpg"><img src="img/pi-adapter-irl.jpg" width="300px"></a>


A single APA102 strip connected to the board:

[![Spixels simple][run-vid]](http://youtu.be/HAbR64yrjUk)

This is used in the [FlaschenTaschen] project, in which only 9 of the 16
connectors are used, one for each 'crate column'. The update rate with
WS2801 reaches 160fps!.

![](img/flaschen-taschen.jpg)

[FlaschenTaschen]: https://github.com/hzeller/flaschen-taschen
[run-vid]: ./img/spixels-video.jpg
