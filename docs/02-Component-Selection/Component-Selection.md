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
| ![](image1.png)<br>Option 1.<br> XC1259TR-ND surface mount crystal<br>$1/each<br>[link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)                 | \* Inexpensive[^1]<br>\* Compatible with PSoC<br>\* Meets surface mount constraint of project                                               | \* Requires external components and support circuitry for interface<br>\* Needs special PCB layout. |
| ![](image3.png)<br>\* Option 2. <br>\* CTX936TR-ND surface mount oscillator <br>\* $1/each <br>\* [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940) | \* Outputs a square wave <br>\* Stable over operating temperature <br> \* Direct interface with PSoC (no external circuitry required) range | * More expensive <br>\* Slow shipping speed                                                         |

*Table 1:*

**Speaker Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](image1.png)<br>Option 1.<br> XC1259TR-ND surface mount crystal<br>$1/each<br>[link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)                 | \* Inexpensive[^1]<br>\* Compatible with PSoC<br>\* Meets surface mount constraint of project                                               | \* Requires external components and support circuitry for interface<br>\* Needs special PCB layout. |
| ![](image3.png)<br>\* Option 2. <br>\* CTX936TR-ND surface mount oscillator <br>\* $1/each <br>\* [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940) | \* Outputs a square wave <br>\* Stable over operating temperature <br> \* Direct interface with PSoC (no external circuitry required) range | * More expensive <br>\* Slow shipping speed                                                         |

### Style 2

> Also acceptable, more markdown friendly

**External Clock Module**

1. XC1259TR-ND surface mount crystal

    ![](image1.png)

    * $1/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Inexpensive                               | Requires external components and support circuitry for interface |
    | Compatible with PSoC                      | Needs special PCB layout.                                        |
    | Meets surface mount constraint of project |

1. CTX936TR-ND surface mount oscillator

    ![](image3.png)

    * $1/each
    * [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Outputs a square wave                                             | More expensive      |
    | Stable over operating temperature                                 | Slow shipping speed |
    | Direct interface with PSoC (no external circuitry required) range |

**Choice:** Option 2: CTX936TR-ND surface mount oscillator

**Rationale:** A clock oscillator is easier to work with because it requires no external circuitry in order to interface with the PSoC. This is particularly important because we are not sure of the electrical characteristics of the PCB, which could affect the oscillation of a crystal. While the shipping speed is slow, according to the website if we order this week it will arrive within 3 weeks.
