---
title: Component Selection Example
---

## Examples

*Table 1:*

**DAC Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://github.com/JaxonBG/JaxonBG_EGR304_F2x.github.io/blob/5832e9aada04e51ba88e56e98312d493174db3a3/docs/02-Component-Selection/MFG_150~C04-018~P%2CPA~8_sml(200x200).webp)<br>Option 1.<br> MCP4921-E/P<br>$2.81/each<br>[link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP4921-E-P/716280)                 | \- 12-bit resolution<br>\- SPI interface<br>\- Through-hole PDIP-8 package<br>\- 2.7 V to 5.5 V operation<br>\- Fast shipping speed                                               | \- Requires external reference voltage<br>\- High unit price |
| ![](https://github.com/JaxonBG/JaxonBG_EGR304_F2x.github.io/blob/8a53ec9fd99018947c0953a123851371127fc1dd/docs/02-Component-Selection/MFG_150~C04-018~P%2CPA~8_sml(200x200).webp)<br>\ Option 2. <br>\ MCP4801-E/P <br>\ $1.61/each <br>\ [Link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP4801-E-P/2332804?s=N4IgTCBcDaILIGEAKAWAHABgIwFoCiA9EiALoC%2BQA) | \- Easier implementation <br>\- Through-hole PDIP-8 <br> \- SPI interface<br>\- Fast shipping speed | - Lower waveform quality <br>\- 8-bit resolution <br>\- More quantization noise                                                       |

**Choice:** Option 1: MCP4921-E/P DAC

**Rationale:** The MCP4921 was chosen because it provides 12-bit resolution. This allows the microcontroller to generate smoother and more accurate analog waveforms for the alarm/ speaker. It also uses SPI communication, which is supported by the PIC18F57Q43, which will make it easy to integrate into the system while keeping fast data transfer. The through-hole PDIP package also simplifies PCB assembly and soldering, since I would I am not the greatest at soldering. 

*Table 1:*

**Audio Amplifier Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://github.com/JaxonBG/JaxonBG_EGR304_F2x.github.io/blob/859a3b1081e82c4aaa314783000e0cb597184415/docs/02-Component-Selection/LM386N-3.webp)<br>Option 1.<br> LM386N-3/NOPB audio amplifier<br>$1.18/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/LM386N-3-NOPB/148191)                 | \* Designed for speakers<br>\* Through-hole PDIP-8<br>\* Operates from 4–12 V                                               | \* Requires capacitors<br>\* Audio quality not as good as modern Class-D amps |
| ![](https://github.com/JaxonBG/JaxonBG_EGR304_F2x.github.io/blob/43a50bd5e8160313164d8cd8b308623d1a6ed633/docs/02-Component-Selection/LM358N.jpg)<br>\* Option 2. <br>\ LM358N audio amplifier <br>\ Price not shown <br>\* [Link to product](https://www.digikey.com/en/products/detail/rochester-electronics-llc/LM358N/11552028) | \- Through-hole DIP-8 <br>\- Wide power supply range <br> \- Suitable for battery operation (if as a group we decide to use that) | - Not an audio amplifier <br>\- Slow shipping speed and non-refundable<br>\- no price shown on Digikey                                                        |

**Choice:** Option 1: LM386N-3 audio amplifier 

**Rationale:** The LM386 was chosen because it is designed for audio amplification and can directly drive an 8 Ω speaker from a 5 V supply which is very helpful since I will not need to introduce another power supply. This makes it a practical choice for increasing the output power of the DAC signal so that the alarm can be heard clearly. Lastly, the DIP package is easy to solder (I am not good at soldering) and is very commonly used in audio projects so I will be able to access resources on the part if I am having any trouble with this part during construction.  

*Table 1:*

**Speaker Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://github.com/JaxonBG/JaxonBG_EGR304_F2x.github.io/blob/1ce5ec4aa75fb066f108e4bb1e2758fab9d07b50/docs/02-Component-Selection/ADS01008MR.jpg)<br>Option 1.<br> ADS01008MR-LW100-R speaker<br>$2.77/each<br>[link to product](https://www.digikey.com/en/products/detail/pui-audio-inc/ADS01008MR-LW100-R/12152292)                 | \- Perfect for simple alarm tones and beeps<br>\- Smaller footprint (10 mm diameter)<br>\- 0.5 W rated power                                               | \- Limited frequency range (1500 Hz to 6000 Hz)<br>\- Will Not very loud (82 dB SPL) |
| ![](image3.png)<br>\ Option 2. <br>\CMS-23558N-L152 speaker <br>\ $6.07/each <br>\ [Link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/CMS-23558N-L152/6137736) | \- Wide frequency response (440 Hz to 20 kHz)<br>\- Very good sound quality <br> \- Fast shipping speed | - Way More expensive <br>\- Larger Footprint<br>/ - Requires more amplifier power                                                         |


**Choice:** Option 2: CMS-23558N-L152 speaker

**Rationale:** The CMS-23558N-L152 was chosen because it can produce a louder and clearer alarm signal. As well as, support a much wider frequency range than the other speaker. The 8 Ω impedance is compatible with the LM386 amplifier, and the larger speaker size allows for improved sound quality but will result in a larger footprint, but I believe that it is a challenge I am willing to take for the better performance. The increased cost is also a con, but I believe that the pros of the speaker outweigh that con. 
