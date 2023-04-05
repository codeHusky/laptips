# Understanding Display Specs
Displays are a tricky thing to understand, mainly because there's a lot of terminology involved that isn't well understood by the greater public. This page should break down the basics of understanding the various specs and features you see talked about with displays.

---

## Bit Depth
Displays all support varied levels of "Bit depth," the most common of which is 8-bit. This "bit depth" defines how much data is allotted per pixel for selecting a color. In essence, higher bit depth values provide larger ranges of color for monitors. 

The formula for this is `x^8=y`, where `x` is the number of bits and `y` is the number of shades. For example, 8-bit color supports 256 shades. Since this is an exponential function, it's notable that 10-bit color is a signficiant upgrade in color range at 1024 shades - literally 4x the maximum color range of 8-bit. However, **bit depth does not mean the panel can discernably display every color in its range.**

Some low-end displays have only 6-bit color with only 64 shades, but often they appear better than they otherwise would because these panels can employ "FRC" technology to display some intermediate shades. This will result in them reporting as 8-bit panels on many operating systems when they are not. The easiest way to tell is to look for a "noise" pattern in solid colors displayed on your screen - if that's present, it's likely your panel is using FRC.

---

## Calibration
Not all displays are created equal. Each different model of display panel displays color slightly different than others, which can result in differing shades of color depending on where you look. Factory calibration can be useful for this reason, ensuring your seeing content as close to the intended range of colors as possible.

It's worth noting that some "factory calibrated" laptop displays will sometimes appear to be washed out or have a strange yellow or blue color tint to all content. This is due to them being calibrated for specific color proofing use. In these situations, it's always possible to switch off the calibration if you'd prefer the more vibrant, while less accurate, color range.

Turning off a calibration in a factory calibrated Windows laptop requires a bit of messing around with Window's color management tools. You basically need to create a new "color profile" with just the default sRGB profile. There's plenty of guides online for this, though, so just look one up for your current OS.

---

## Color
There are quite a few different standards for color that all have different names and have differing levels of relevance and meaning to the average consumer. Each of these standards defines a range of colors, referred to as "color gamuts." 

For simple charts for comparing various color gamuts and color spaces, use [this website](https://www.saji8k.com/displays/color-space/rec-709/).

#### NTSC
NTSC is largely irrelevant in modern monitors despite being a common point of comparison for color coverage. Some monitors will tout numbers like "45% NTSC" or "90% NTSC" as one of their gamut specs, providing good context for the added range of color that monitor may provide over your current one.

However, next to zero content is mastered for NTSC and it's not a useful thing to look in most cases. It's only really useful in a "is this building taller or shorter than the trees" sense.

#### sRGB/Rec. 709
**If you're looking for a screen for watching SDR media, you should look for 100% sRGB coverage.**

sRGB, or the "standard RGB color space," is a standard defined in 1996 by HP and Microsoft. This is the color gamut that is accepted as "web color," and includes a limited range of the RGB color space.

sRGB is functionally identical to the Rec. 709, but is a more specific standard targeted at TVs and mastering for SDR content for shows and movies. For this reason, 100% sRGB gives you the best chance at watching movies and TV on your device as intended.

Having 100% sRGB coverage guarantees at least 78% NTSC coverage, 85% Adobe RGB coverage, and 79% DCI P3 coverage. Values higher than this paired with sRGB 100% indicate higher color coverage than average.

#### Adobe RGB
**If you're looking for a screen for color work, you should look for high Adobe RGB coverage.**

Less frequently mentioned by manufacturers, Adobe RGB is a colorspace targeting most colors visible on CMYK printers. This makes it a very useful range to look for high coverage of if you plan on using your device for anything that requires print color accuracy.

Coverage of 100% of the Adobe RGB gamut provides 100% sRGB coverage automatically, while covering 92% of NTSC and 87% of DCI P3.

#### DCI P3
**If you're looking for a screen for watching HDR media, you should look for high DCI P3 coverage.**

DCI P3 is a "digital cinema projector" color space. Projectors used in theaters support this color space in its entirety. Few displays support this range in its entirety, mostly at the high end of price ranges.

DCI P3 is an HDR color range. If your display is advertised as having high DCI P3 color coverage, you can likely consume HDR content on it.

Coverage of 100% of the DCI P3 gamut provides 100% sRGB coverage automatically, while also covering 90% of NTSC and 93% of Adobe RGB.

---
## Refresh Rate
Refresh rate indicates how many times a panel can update its pixels per second. For example, a 60hz display can update its pixels 60 times a second, and a 300hz panel can update its pixels 300 times a second.

Higher refresh rate panels can make many animations feel far more fluid in the OS, as well as make the overall user experience on a system feel far better than it might otherwise be. They can also make devices feel more "responsive" than they otherwise may feel, but this is just a perceived effect.

For gaming, a high refresh rate monitor may be preferable in order to gain an edge over other players in competitive scenarios. For others, it may be to simply have a better experience on their computer. Regardless, everyone looking for good, high refresh rate displays cares (whether they know or not) about low Response Times.

---

## Response Times
Response time is the amount of time it takes a pixel on a given display to transition from one color to another. If this takes too long, this can result in blurring, smearing, or "ghosting" effects in moving or changing content. This is not only awful for games, but can be distracting in daily usage and multimedia consumption if it's severe enough.

Manufacturers love to tout low responsne time numbers such as 3ms, 5ms, or even >1ms. However, there's a lot more to the story than just the advertised specs. In fact, these numbers are massively misleading.

#### Manufacturer "Response Times"
Traditionally, "rise time measurements" are taken to record response times by panel and laptop manufacturers. These measurements exclude the first and last 10% of the response, meaning that 20% of the overall response is ignored. This is referenced as "T10-90%." The remaining 80% accounts for where the pixel transition ramps up to its highest speeds.

The problem with this stems from the way most display technologies work. Displays spend a lot of time in the excluded 20% of the "response time" beginning and ending their pixel color transitions. What this means is that while 80% of the actual response is recorded, the 20% of the response that's ignored accounts for a large portion of the time spent waiting for the display to update.

Due to this, many manufacturers will opt to use this far more ambiguous T10-90% figure as an indicator of pixel response time. While this is not strictly "wrong" or "false advertising," the numbers used are not useful for consumers whatsoever. Ignoring that 20% results in some "1ms" displays with actual response times that make 60fps content a blurry mess. 

For this reason, you should **generally ignore manufacturer specified response times**. For example, you could, in theory, have a "2ms" panel that has a faster overall response time than a ">1ms" panel because the ">1ms" panel spends 4x longer in the excluded 20% range.

#### Reviewer Response Times
Not all reviewers provide T0-100% response time measurements, but **they should be**. If you're interested to see if a reviewer is properly testing response times, you can compare their data against data from an outlet like [RTINGS.com](https://RTINGS.com) or reputable YouTube reviewers like [Jarrod's Tech](https://www.youtube.com/jarrodstech) and [Hardware Unboxed](https://www.youtube.com/@Hardwareunboxed). Response time numbers are rarely less than 1ms except on extremely high refresh rate panels.

You can determine what the highest "ideal" response time is for your particular display by plugging its refresh rate into this formula: `1000/r`. The reasoning behind this is that there are 1000ms (milliseconds) in every second.

For example, a 60hz monitor should target a response time >=16ms. A 120hz display should target >=8ms, a 165hz should target >=6ms, and a 240hz display should target >=4ms.

As you can see, these numbers are far larger than the numbers touted by manufacturers. They also paint a far clearer picture of which panels are better and worse, and overall are instrumental in comparing products.