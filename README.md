# ADIF Notes

These are @tcort's notes on various ADIF implementations.

| Name | Version | Homepage | Language | Import 7-Bit | Import ISO-8859-1 | Import Unicode | Counting Method | Export 7-Bit | Export ISO-8859-1 | Export Unicode |
|------|---------|----------|----------|--------------|-------------------|----------------|-----------------|--------------|-------------------|----------------|
| **SKCCLogger** | `03.01.03` | [http://groups.io/g/SKCCLogger/](http://groups.io/g/SKCCLogger/) | Xojo | Y | Y | N | Unknown | Y | Y | N |
| **tcadif** | `2.2.1` | [https://github.com/tcort/tcadif](https://github.com/tcort/tcadif) | JavaScript | Y | N | N | Characters | Y | N | N |
| **qle** | `2.5.0` | [https://www.va2nw.ca/qle.html](https://www.va2nw.ca/qle.html) | C | N/A | N/A | N/A | Bytes | Y | N | N |

- Want an application tested? Create an issue!
- Want to report on or update the information about an application? Create an issue and/or pull request!
- Want additional information collected? Create an issue!

## Test Files

The `test-files/` directory contains sample files with 7-bit ascii strings, iso-8859-1 strings, and unicode strings. These are hand crafted. Ideally, once I find an application that exports ISO-8859-1 and/or Unicode, I'll use the real world ADIF (rather than my contrived examples).
