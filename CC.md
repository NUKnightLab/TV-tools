# Closed Captions

Changes and developments in recent years in the space of technologies related to "television" (broadly speaking) have narrowed rather than widened the technical accessibility (which is to say the hackability) of closed caption feeds.

Closed caption technology itself is a bit of a hack into the video layer of standard broadcast formats (e.g. NTSC and PAL). As the industry has moved more toward streaming formats, this hacked-in technology has gradually given way to more proprietary approaches to managing captions which tend to operate in those services more as traditional "subtitles" have rather than "captions".

These changes affect not only the typical services that come to mind with respect to streaming (Netflix, Amazon Prime, all things Roku, smart television, etc.) but also affect what are thought of as more traditional forms like cable distribution. For example, a bit more research is required to verify this, but it appears that Xfinity does not transmit the CC feed through its converter boxes. Rather, CC on Xfinity cable is supported internal to the box itself and that data is not accessible through standard CC signal extraction from the video signal. It also seems that HDMI (the connection standard that has largely replaced component RCA jacks) does not transmit the CC data.

## So what does work?

For the above stated reasons, the tools here focus on previous generation technology. Specifically, local television broadcast is utilized (digital broadcast only per somewhat recent FCC changes). The resource stack then requires a digital broadcast antenna, a television tuner, a setup for extracting closed captions, and a television to monitor the results.

## The technology

We have used the following suite of tools for extracting closed captions from broadcast television feeds. This has been done as a proof-of-concept to prove out the idea. The results are iffy, but usable for certain limited use cases. The code used, and a sample transcript is provided as described below.

### The tools

 * [AntennaDigital HDTV Antenna with cable-integrated signal amplifier](https://www.amazon.com/gp/product/B0768T6DZ5/)
 * [1byone ATSC digital converter box](https://www.amazon.com/gp/product/B01N5MLC1M/)
 * [Arduino Uno](https://store.arduino.cc/usa/arduino-uno-rev3)
 * [Nootropic Video Experimenter Arduino Shield](https://nootropicdesign.com/store/product/video-experimenter-assembled/)
 * Laptop computer
 
### Code and results

The code used to prove out extraction of closed captions was taken directly from the Nootropic examples. Project description and code download can be found [here](http://nootropicdesign.com/projectlab/2011/03/20/decoding-closed-captioning/)

Notable changes to that code include:

 * The CC signal seemed to be clearer on NTSC line 22 rather than the specified 21 or 13 as used in the example code
 * A data capture start value of 311 showed a small improvement over the example value of 310
 
The modified code used is here



