# ADIF Notes

Many of the recent discussions in the [adifdev](https://groups.io/g/adifdev/) group around character encoding explore the impacts on existing ADIF implementations and the ability of existing implementations to adapt to support different encoding schemes. I'm attempting to collect relevant information so that we can make more informed decisions on the topic. I've set up a github repository where I will post the information that I find. It will allow others to collaborate if they want to help and/or raise issues (e.g. an additional ADIF implementation to examine).

## Character Set Handling

| Name | Version | Homepage | Language | Import 7-Bit | Import ISO-8859-1 | Import Unicode | Counting Method | Export 7-Bit | Export ISO-8859-1 | Export Unicode | Non-representable Data |
|------|---------|----------|----------|--------------|-------------------|----------------|-----------------|--------------|-------------------|----------------|----------------------|
| **ACLog** | `7.0.11` | [https://www.n3fjp.com/aclog.html](https://www.n3fjp.com/aclog.html) | Unknown | Y | Y | Y | Unknown | Y | N | N | non-7bit ASCII and Unicode characters export as `?`. |
| **MacLoggerDX** | `6.57` | [https://www.dogparksoftware.com/MacLoggerDX.html](https://www.dogparksoftware.com/MacLoggerDX.html) | Unknown | Y | Y | N | Unknown | Y | N | N | Export replaces Unicode with `?` (e.g. `❤️` becomes `?`) and strips accents on export (e.g. `é` becomes `e`). Import rejects UTF8 in String fields. |
| **qle** | `2.5.0` | [https://www.va2nw.ca/qle.html](https://www.va2nw.ca/qle.html) | C | N/A | N/A | N/A | Bytes | Y | N | N | Omits fields containing non-7bit ASCII data from export. |
| **SKCCLogger** | `03.01.03` | [http://groups.io/g/SKCCLogger/](http://groups.io/g/SKCCLogger/) | Xojo | Y | Y | N | Unknown | Y | Y | N | Input widgets don't accept UTF8. |
| **tcadif** | `2.2.1` | [https://github.com/tcort/tcadif](https://github.com/tcort/tcadif) | JavaScript | Y | N | N | Characters | Y | N | N | Refuses to import/export non-7bit ASCII data. |

- Want an application tested? Create an issue!
- Want to report on or update the information about an application? Create an issue and/or pull request!
- Want additional information collected? Create an issue!

## Test Files

The `test-files/` directory contains sample files with 7-bit ascii strings, iso-8859-1 strings, and unicode strings. These are hand crafted. Ideally, once I find an application that exports ISO-8859-1 and/or Unicode, I'll use the real world ADIF (rather than my contrived examples).

## Results

The `results/` directory contains ADIF output from various applications.
