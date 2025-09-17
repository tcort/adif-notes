# ADIF Notes

Many of the recent discussions in the [adifdev](https://groups.io/g/adifdev/) group around character encoding explore the impacts on existing ADIF implementations and the ability of existing implementations to adapt to support different encoding schemes. I'm attempting to collect relevant information so that we can make more informed decisions on the topic. I've set up a github repository where I will post the information that I find. It will allow others to collaborate if they want to help and/or raise issues (e.g. an additional ADIF implementation to examine).

## Goal

The goal of this project is to survey existing ADIF implementations to answer the following questions:

 - how common is it for implementations to import/export out of spec Strings (e.g. extended ASCII, Unicode, etc)?
 - how do existing ADIF implementations calculate the length of String data: counting bytes or counting characters?
 - which programming languages are used to implement ADIF?
 - how common is support for ADX?

## Character Set Handling

| Name | Version | Homepage | Language | Import 7-Bit | Import ISO-8859-1 | Import Unicode | Counting Method | Export 7-Bit | Export ISO-8859-1 | Export Unicode | Comments | Supports ADX |
|------|---------|----------|----------|--------------|-------------------|----------------|-----------------|--------------|-------------------|----------------|----------|--------------|
| **ACLog** | `7.0.11` | [https://www.n3fjp.com/aclog.html](https://www.n3fjp.com/aclog.html) | Unknown | ✅ | ✅ | ✅ | Characters | ✅ | ❌ | ❌ | non-7bit ASCII and Unicode characters export as `?`. Imported heart emoji properly in `<NAME:1>❤️` so assume it is counting characters rather than bytes. | ❌ |
| **HAMRS Pro** | `2.44.0` | [https://hamrs.app/](https://hamrs.app/) | Unknown | ✅ | ✅ | ✅ | Bytes | ✅ | ✅ | ✅ | Outputs `<NOTES:2>❤️` so assume it's counting bytes. | ❌ |`
| **klog** | `2.5-RC1` | [https://github.com/ea4k/klog](https://github.com/ea4k/klog) | C++ | ✅ | ✅ | ✅ | Bytes | ✅ | ✅ | ✅ | Output includes `<NAME:2>❤️` so assume it is counting bytes. | ❌ |
| **MacLoggerDX** | `6.57` | [https://www.dogparksoftware.com/MacLoggerDX.html](https://www.dogparksoftware.com/MacLoggerDX.html) | Unknown | ✅ | ✅ | ❌ | Unknown | ✅ | ❌ | ❌ | Export replaces Unicode with `?` (e.g. `❤️` becomes `?`) and strips accents on export (e.g. `é` becomes `e`). Import rejects UTF8 in String fields. | ✅ |
| **qle** | `2.5.0` | [https://www.va2nw.ca/qle.html](https://www.va2nw.ca/qle.html) | C | N/A | N/A | N/A | Bytes | ✅ | ❌ | ❌ | Omits fields containing non-7bit ASCII data from export. | ❌ |
| **RumLogNG** | `5.19.5` | [https://www.dl2rum.de/rumsoft/RUMLog.html](https://www.dl2rum.de/rumsoft/RUMLog.html) | Unknown | ✅ | ✅ | ✅ | Bytes | ✅ | ✅ | ✅ | Exports `<comment:2>❤️` so assume it's counting bytes rather than characters. | ✅ |
| **SKCCLogger** | `03.01.03` | [http://groups.io/g/SKCCLogger/](http://groups.io/g/SKCCLogger/) | Xojo | ✅ | ✅ | ❌ | Unknown | ✅ | ✅ | ❌ | Input widgets don't accept UTF8. | ❌ |
| **tcadif** | `2.2.1` | [https://github.com/tcort/tcadif](https://github.com/tcort/tcadif) | JavaScript | ✅ | ❌ | ❌ | Characters | ✅ | ❌ | ❌ | Refuses to import/export non-7bit ASCII data. | ❌ |

- Want an application tested? Create an issue!
- Want to report on or update the information about an application? Create an issue and/or pull request!
- Want additional information collected? Create an issue!

## Methodology -- how to fill in the table above

- Import
 - 7-bit - Strings with Characters in the range 32 to 126 (inclusive) can be imported
 - ISO-8859-1 - Strings with single byte Characters outside the range 32 to 126 (inclusive) can be imported (e.g. `é`)
 - Unicode - Strings with multibyte unicode characters can be imported (e.g. `❤️`)
- Counting Method - how length is determined. Inferred by examining the exported length for a single multibyte unicode character and/or inferred by examining an imported string. Can also be determined by source code inspection.
 - Bytes - example: seeing the 2 for a single unicode character in the output. `<NAME:2>❤️` 
 - Characters - example: successfully importing a multibyte unicode character when the length specifier is 1. `<NAME:1>❤️`
 - Unknown - example: it cannot be determined which method is used (e.g. it only imports/exports single byte characters and source code is unavailable).
- Export
 - 7-bit - Strings with Characters in the range 32 to 126 (inclusive) can be exported
 - ISO-8859-1 - Strings with single byte Characters outside the range 32 to 126 (inclusive) can be exported (e.g. `é`)
 - Unicode - Strings with multibyte unicode characters can be exported (e.g. `❤️`)
- Comments
 - how was the length counting method determined.
 - what does a multibyte unicode character look like when exported.
 - etc.

## Test Files

The `test-files/` directory contains sample files with 7-bit ascii strings, iso-8859-1 strings, and unicode strings. These are hand crafted. Ideally, once I find an application that exports ISO-8859-1 and/or Unicode, I'll use the real world ADIF (rather than my contrived examples).

## Results

The `results/` directory contains ADIF output from various applications.
