# Extended test results

Based on the files described in [test-files/README.md](test-files/README.md).

# Summary (more details below)

| App                | Enc  | ISO | UTFb | UTFc | UI   | Exp  | ADX |
|--------------------|------|-----|------|------|------|------|-----|
| AALog              | 8️⃣  | ✅   | ✅�   | 🟡�  | 8️⃣  | 8️⃣  | ❌   |
| ADIF Master        | 8️⃣  | ✅   | ✅�   | 🟡�  | 8️⃣  | 8️⃣  | ❌   |
| ClubLog            | ?    | ✅   | ✅    | ✅    | ?    | ?    | ❌   |
| DXKeeper           | 8️⃣  | ✅   | ✅�   | 🟡�  | 8️⃣  | 8️⃣  | ❌   |
| DXLog.net          | 🇺🇳 | ✅   | ❌    | ✅    | 🇺🇳 | 💾s  | ❌   |
| Fast Log Entry     | ?    | ?   | ?    | ?    | ?    | 💾s  | ❌   |
| Hamlog.online      | 🇺🇳 | ✅�  | ✅    | 🟡�  | 🇺🇳 | 8️⃣s | ❌   |
| Ham Radio Deluxe   | 🇺🇳 | ✅   | ✅�   | 🟡�  | 🇺🇳 | 8️⃣t | 🟡  |
| HAMRS Pro          | 🇺🇳 | ✅�  | ✅    | ✅    | 🇺🇳 | 🇺🇳 | ❌   |
| Log4OM             | 🇺🇳 | ✅�  | ✅    | ✅    | 🇺🇳 | 🇺🇳 | ❌   |
| Logger32           | 8️⃣  | ✅   | ✅�   | 🟡�  | 8️⃣  | 8️⃣  | ❌   |
| MacLogger DX       | 🇺🇳 | ✅�  | ✅    | 🟡   | 🇺🇳 | 💾s  | 🟡  |
| N1MM+              | 🇺🇳 | ✅�  | ❌    | ✅    | 🇺🇳 | 8️⃣t | ❌   |
| N3FJP              | 🇺🇳 | ✅�  | 🟡   | ✅    | 🇺🇳 | 8️⃣t | ❌   |
| POTA               | ?    | ✅   | ✅    | ✅    | ?    | ?    | ❌   |
| QRZ.com            | 🇺🇳 | ✅�  | ✅    | ✅    | 🇺🇳 | 🇺🇳 | ❌   |
| RumLogNG           | 🇺🇳 | ✅   | 🟡   | ✅    | 🇺🇳 | 🇺🇳 | 🟡  |
| SOTA               | ?    | ✅   | ❌    | ✅    | ?    | ?    | ❌   |
| Swisslog           | 8️⃣  | ✅   | ✅�   | 🟡�  | 8️⃣  | 💾s  | ❌   |
| WinLog32           | 8️⃣  | ✅   | ✅�   | 🟡�  | 8️⃣  | 8️⃣  | ❌   |
| World Radio League | 🇺🇳 | ✅�  | ✅    | ✅    | 🇺🇳 | 🇺🇳 | ❌   |


Columns:
* `Enc`: Internal encoding: 8️⃣ ISO-8859-1, 🇺🇳 Unicode
* `ISO`: Can import ISO-8859-1. � misencoded
* `UTFb`: Can import Unicode, byte counts. � misencoded, 🟡 with extra bytes, ❌ missing fields or records
* `UTFc`: Can import Unicode, character counts. � misencoded, 🟡 truncated strings, ❌ missing fields or records
* `UI`: User Interface encoding
* `Exp`: Can export 💾: ASCII, 💾s: ASCII sanitized, 8️⃣: Raw ISO-8859-1 (or Unicode with byte counts), 8️⃣s: Sanitized ISO-8859-1, 8️⃣t: Transcoded ISO, 🇺🇳: Unicode, character counts
* `ADX`: Supports ADX. 🟡 no _INTL fields

# Other Apps

| App                                                | Status                       |
|----------------------------------------------------|------------------------------|
| 59+ Log                                            | Discontinued                 |
| ADIF to Excel or Excel to ADIF                     | Discontinued (2013?)         |
| Aether Logbook                                     | Requires purchase ($40)      |
| BBLogger                                           | Could not find download link |
| Cabrillo Criollo LU4EG                             | Could not find download link |
| CheckLog                                           | Instructions in Russian      |
| CQRLOG                                             | Requires Linux               |
| DX4Win                                             | Coult not get it to import   |
| DXBase                                             | Website is dead              |
| DXtreme Station Log                                | Requires purchase ($80)      |
| Easy Log                                           | Could not find download link |
| Ham-LCT                                            | Discontinued                 |
| [HLog](https://www.josefsipek.net/projects/hlog/)  | -                            |
| [ZZALog](https://sourceforge.net/projects/zzalog/) | -                            |
| Writelog                                           | -                            |
| Ham Office                                         | -                            |
| HamLog                                             | -                            |
| Ham Support                                        | -                            |
| Journal                                            | -                            |
| KLog                                               | -                            |
| LOGic 9                                            | -                            |
| NewLogOSH                                          | -                            |
| Pignology                                          | -                            |
| Shacklog                                           | -                            |
| TurboLog                                           | -                            |
| Ucxlog                                             | -                            |
| VQLog                                              | -                            |
| XLog                                               | -                            |
| XMLog                                              | -                            |
| YPLog                                              | -                            |


Columns:
* `Enc`: Internal encoding
* `Imp ISO`: Can import ISO-8859-1
* `Imp UTF`: Can import Unicode
* `UI`: User Interface encoding
* `Exp ISO`: Can export ISO-8859-1
* `Exp UTF`: Can export Unicode
* `Under`: Can recover from fields with count shorter than available data (can truncate and lose data).
* `Over`: Can recover from fields with count longer than available data.
* `Ent`: Decodes entities
* `ADX`: Supports ADX

Values:
* `U`: UTF-8, `I`: ISO-8859-1
* `trans`: uses transcoding, `sanit`: uses sanitization
* `chars`: character counts, `bytes`: byte counts
* `intl`: uses _INTL fields, `no intl`: does not use _INTL fields


# Detailed Results
⁉️ Indicates unexpected findings.
🥳 Indicates unexpected positive findings.
😭 Indicate unexpected negative findings.

---

---

### [AALog](https://www.dxsoft.com/en/products/aalog/) - Limited Testing

**Version:** 3.9.0 build 1288

**Tested:** 2025-09-23 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.

This app seems to:

* Use ISO-8859-1 internally
* Count ADIF field in bytes

---

### [ADIF Master](https://www.dxsoft.com/en/products/adif-master/) - Limited Testing

**Version:** 3.6

**Tested:** 2025-09-23 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.

This app seems to:

* Use ISO-8859-1 internally
* Count ADIF field in bytes

---

### [ClubLog](https://clublog.org/) - Limited Testing

**Version:** N/A

**Tested:** 2025-09-23 by KI2D

* Imported a QSO with UTF-8 sequences and count in bytes: ✅
* Imported a QSO with UTF-8 sequences and count in characters: ✅

The app does not import any String fields so we cannot describe how it handles them.

It does, however, seem to be able to handle field counts in bytes and characters.
Meaning it either uses UTF-8 and can also handle overcount, or more likely it uses ISO-8859-1 and can handle undercount.

---

### [DXKeeper](https://www.dxlabsuite.com/dxkeeper/)

**Version:** 18.1.4

**Tested:** 2025-09-19 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 4:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 5:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 7:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accented char displayed correctly, but entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake, entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 13:** 🟡 Accented characters displayed correctly, emoji converted to question mark.
* **Test 14:** 🟡 DO6JJ name transcoded to "Jorg". 🟡 EA7GXD QTH transcoded to "Malaga". ZP5DA QTH transcoded to "Asuncion"

Exports:
* ADIF Export: encoded as ISO-8859-1, with field counts in bytes, one space between fields, CRLF between records. "Mojibake" preserved on export.

Notes: Import functionality has an option for "non-compliant ADIF", but it does not seem to make any difference in these results.

This app seems to:

* Use ISO-8859-1 or Win-1252 internally
* Count ADIF field in bytes
* Handle fields with data beyond length (undercount)
* Not transcode UTF-8 when importing
* Not transcode HTML entities when importing
* Correctly limit UI input to ISO-8859-1
* Transcode lookup data 🥳, as 7-bit ASCII

---

### [DXLog.net](https://dxlog.net/)

**Version:** 2.6.10

**Tested:** 2025-09-27 by KI2D

ADIF import does not include any String fields so we cannot describe how it handles them.

Only UI element we could use was "Operator Name" in contest setting. It accepted accented characters and emoji.
But ADIF export had those replaced with `?`.

* **Test 4:** ❌ Failed to import QSO.
* **Test 5:** ✅ Imported QSO.

This app seems to:

* Use Unicode internally
* Count ADIF field in characters
* Fail to handle fields with length past data (overcount)
* Correctly accept Unicode input in the UI
* Sanitize Unicode on export to 7-bit ASCII with '?'

---

### [Fast Log Entry](https://df3cb.com/fle/download/)

**Version:** 3.4

**Tested:** 2025-09-27 by KI2D

No ADIF import.

Exports ADIF as sanitized 7-bit ASCII.

---

### [Hamlog.online](https://hamlog.online/)

**Version:** N/A

**Tested:** 2025-09-20 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data misdecoded. Greek codepage?
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accents loaded, but not upcased with rest of string
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 4:** ❌ Failed to import QSO.
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data truncated, and some characters misdecoded?
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Data displayed correctly, but upcased.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Data displayed correctly, but upcased.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data misdecoded. Entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accents decoded, but entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data misdecoded. Entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 13:** ✅ Data displayed correctly. Not upcased.
* **Test 14:** 🔲 Does not support QRZ.com lookups.


Exports:
* ADIF Export: Somehow cleaned into ISO-8859-1 with all UTF characters replaced with `?`, count in bytes, no spaces between fields, CRLF between records.

This app seems to:

* Use Unicode internally.
* Count ADIF fields in bytes, not characters.
* Handle fields with data beyond length (undercount)
* Does not handle fields with length shorter than data (overcount)
* Transcode ISO-8859-1 using some different codepage. Accented `á` shows up as `б` (delta) and `ñ` shows up as `с`.
* Not transcode HTML entities when importing
* Remove UTF byte sequences on export, but preserve non-UTF byte sequences
* Correctly accept Unicode input in the UI

---

## [Ham Radio Deluxe Logbook](https://hamradiodeluxe.com/)

**Version:** 6.8.0.372

**Tested:** 2025-09-20 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 4:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 5:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 7:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly. entities decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accented characters as mojibake, but entities decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 13:** ✅ Data displayed correctly. ❌ But dropped on export ⁉️
* **Test 14:** 🟡 DO6JJ name transcoded to "Jorg". 🟡 EA7GXD QTH transcoded to "Malaga". ZP5DA QTH transcoded to "Asuncion"

Exports:
* ADIF Export: transcoded to ISO-8859-1, with field counts in bytes, one space between fields, CRLF between records. But manually entered QSO with emoji, even if displayed correctly, was exported as <name:0>
* ADX Export: As UTF-8, does NOT use _INTL fields.

Notes: Import functionality has an option for "non-compliant ADIF", but it does not seem to make any difference in these results.

This app seems to:

* Use ISO-8859-1 internally? Or maybe Unicode? And only converted on display?
* Interpret all ADIF imports as ISO-8859-1.  Maybe transcode internally?
* Transcode HTML entities 🥳 to Unicode??? but maybe only on display?
* Count ADIF field in bytes
* Handle fields with data beyond length (undercount)
* Not transcode UTF-8 when importing
* Correctly accept Unicode input in the UI, but dropped on export
* Correctly accept Unicode data on lookup, maybe transcode internally?

---

### [HAMRS Pro](https://hamrs.app/)

**Version:** 2.44.0

**Tested:** 2025-09-27 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with �.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* Skipped other tests since their results are predictable by tests 1-4.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** ✅ Data displayed correctly.

Imports ADIF as separate logbooks, so no we could not capture a useful screenshot or export showing all records.

Exports:
* ADIF Export: encoded as UTF-8, field counts in characters, CRLF between fields, two CRLF between records.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use Unicode internally
* Count ADIF field in characters
* Handle fields with data beyond length (undercount)
* Handle fields with length past data (overcount)
* Not transcode when importing or exporting
* Correctly accept Unicode input in the UI

---

### [Log4OM](https://www.log4om.com/)

**Version:** 2.36.1.0

**Tested:** 2025-09-21 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with �.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Data displayed correctly, entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 12.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 11.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** ✅ Data displayed correctly.

Exports:
* ADIF Export: encoded as UTF-8, includes BOM, field counts in characters, one space between fields, two CRLF between records.
* There's an option to export "Export Standard ADIF", but this still uses UTF-8 encoding and character counts.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use Unicode internally
* Count ADIF field in characters
* Handle fields with data beyond length (undercount)
* Handle fields with length past data (overcount)
* Not transcode when importing or exporting
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI

---

### [Logger32](https://www.logger32.net/)

**Version:** 4.0.307

**Tested:** 2025-09-22 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 4:** ✅ Imported QSO. ✅ Imported all bytes.  ❌ Data displayed as mojibake.
* **Test 5:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 7:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accented char displayed correctly, but entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake, entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 13:** 🟡 Accented characters displayed correctly, emoji converted to question mark.
* **Test 14:** Could not figure out how to configure QRZ lookups.

Exports:
* ADIF Export: encoded as ISO-8859-1, with field counts in bytes, one space between fields, CRLF between records. "Mojibake" preserved on export.

Notes: Import functionality has an option for "non-compliant ADIF", but it does not seem to make any difference in these results.

This app seems to:

* Use ISO-8859-1 or Win-1252 internally
* Count ADIF field in bytes
* Handle fields with data beyond length (undercount)
* Not transcode UTF-8 when importing
* Not transcode HTML entities when importing
* Correctly limit UI input to ISO-8859-1

---

### [MacLogger DX](https://www.dogparksoftware.com/MacLoggerDX.html)

**Version:** 6.57

**Tested:** 2025-09-27 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Transcoded to unknown code page.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Transcoded to unknown code page.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Data displayed correctly, entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Transcoded to unknown code page, and entities not decoded.
* **Test 11:** 🟡 Processed as with Test 1, autodetected ISO-8859-1.
* **Test 12:** 🟡 Processed as with Test 1, autodetected ISO-8859-1.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** ✅ Data displayed correctly.

Exports:
* ADIF Export: encoded as 7-bit ASCII, with sanitization and simplification, field counts in bytes, one space between fields, two CRLF between records.
* ADX Export: encoded as UTF-8, but data originally in ISO-8859-1 shows up as unexpected mojibake. No _INTL fields.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use Unicode internally
* Count ADIF field in characters
* Handle fields with data beyond length (undercount)
* Handle fields with length past data (overcount), dropping fields.
* Transcode non-UTF but not sure of which codepage.
* Sanitize on export to ADI.
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI

---

### [N3FJP Amateur Contact Log](https://www.n3fjp.com/aclog.html)

**Version:** 7.0.11

**Tested:** 2025-09-21 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with �.
* **Test 2:** 🟡 Imported QSO, missing fields. 🟡 Missing fields. 🟡 Data displayed correctly, but field data shifted.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** 🟡 Imported QSO, missing even morefields. 🟡 Missing fields. 🟡 Data displayed correctly, but field data
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** 🟡 Imported QSO, missing fields. 🟡 Missing fields. 🟡 Data displayed correctly, but field data shifted.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Data displayed correctly, entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 12.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 11.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** ✅ Data displayed correctly.

Exports:
* ADIF Export: transcoded to ISO-8859-1, invalid UTF-8 sequences replaced with `?`, field counts in bytes, CRLF fields, CRLF between records.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use Unicode internally
* Import ADIF as UTF-8 with character counts
* Export as ISO-8859-1 with transcoding and byte counts.
* Handle fields with data beyond length (undercount)
* Fail to handle fields with length past data (overcount)
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI

---

### [N1MM+](https://www.n1mm.com/)

**Version:** 1.0.10923

**Tested:** 2025-09-20 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with �.
* **Test 2:** ❌ Failed to import QSO.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** ❌ Failed to import QSO.
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** ❌ Failed to import QSO.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly? Missing some korean characters?
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accented char displayed correctly, but entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** 🔲 Does not support QRZ.com lookups.

Exports:
* ADIF Export: Unicode data transcoded to ISO-8859-1 ⁉️, field counts in bytes, one space between fields, CRLF between records.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use Unicode internally
* Count ADIF field in characters on import, transcoding to ISO-8859-1 on export
* Not handle fields with length longer than data (overcount)
* Always imports as UTF-8 and always exports as transcoded to ISO-8859-1, with no autodetection.
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI

---

### [POTA.app](https://pota.app/)

**Version:** N/A

**Tested:** 2025-09-27 by KI2D

ADIF import does not include any String fields so we cannot describe how it handles them.

* Imported a QSO with UTF-8 sequences and count in bytes: ✅
* Imported a QSO with UTF-8 sequences and count in characters: ✅

---

### [QRZ.com](https://www.qrz.com/)

**Version:** N/A

**Tested:** 2025-09-19 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with �.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly, entities decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 12.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 11.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** ❌ DO6JJ name set to "J rg". ❌ EA7GXD QTH set to "MÃÂ¡laga". ❌ ZP5DA QTH set to "AsunciÃ³n"

Exports:
* ADIF Export: encoded as UTF-8, field counts in characters, LF between fields, LF between records.

Notes: Import functionality has no options.

This app seems to:
* Use Unicode internally
* Count ADIF field in characters
* Handle fields with data beyond length (undercount)
* Handle fields with length shorter than data (overcount) 🥳
* Not transcode ISO-8859-1 when importing
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI
* Mis-transcode lookup data, apparently treating UTF-8 source data as ISO-8859-1 and then trying to transcode that to UTF-8 😭

---

### [RumLogNG](https://www.dl2rum.de/)

**Version:** 5.19.4

**Tested:** 2025-09-19 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ❌ Imported extra bytes. ✅ Data displayed correctly.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** ✅ Imported QSO. ❌ Truncated bytes.  🟡 Data displayed correctly (up to truncation).
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** ✅ Imported QSO. ❌ Imported extra bytes. ✅ Data displayed correctly.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accented char displayed correctly, but entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accented char displayed correctly, but entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Entities not decoded.
* **Test 11:** 🟡 Mixed results. ISO-8859-1 data imported correctly, but UTF data imported as mojibake.
* **Test 12:** 🟡 Mixed results. ISO-8859-1 data imported correctly, but UTF data imported as mojibake.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** ✅ DO6JJ name set to "Jörg". 🟡 EA7GXD QTH bytes preserved as mojibake. ✅ ZP5DA QTH set to "Asunción"

Exports:
* ADIF Export: encoded as UTF-8, field counts in characters, one space between fields, CRLF between records.
* ADX Export: encoded as UTF-8, does NOT use _INTL fields.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use Unicode internally
* Count ADIF field in characters
* Handle fields with data beyond length (undercount)
* Handle importing files with different encodings, autodetecting encoding and transcoding if necessary
* Seems to assume that files that have invalid UTF-8 sequences are encoded as ISO-8859-1
* Not transcode HTML entities when importing
* Correctly interpret lookup data as UTF-8

---

### [SOTA.app](https://sotadata.org.uk/)

**Version:** N/A

**Tested:** 2025-09-27 by KI2D

ADIF import does not include any String fields so we cannot describe how it handles them.

* Imported a QSO with UTF-8 sequences and count in bytes: ❌
* Imported a QSO with UTF-8 sequences and count in characters: ✅

---

### [Swisslog](https://www.swisslogforwindows.com/)

**Version:** 5.113

**Tested:** 2025-09-27 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 4:** ✅ Imported QSO. ✅ Imported all bytes.  ❌ Data displayed as mojibake.
* Skipped other tests since their results are predictable by tests 1-4.
* **Test 13:** 🟡 Accented characters displayed correctly, emoji converted to question mark.
* **Test 14:** ✅ Transcoded to ISO-8859-1.

Exports:
* ADIF Export: sanitized as 7-bit ASCII, with field counts in bytes, two spaces between fields, CRLF after certain fields, two CRLF between records.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use ISO-8859-1 internally
* Count ADIF field in bytes
* Handle fields with data beyond length (undercount)
* Not transcode UTF-8 when importing
* Correctly limit UI input to ISO-8859-1


---

### [WinLog32](http://www.winlog32.co.uk/)

**Version:** 7.3.46

**Tested:** 2025-09-27 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 2:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 3:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 4:** ✅ Imported QSO. ✅ Imported all bytes.  ❌ Data displayed as mojibake.
* **Test 5:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 6:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake.
* **Test 7:** ✅ Imported QSO. ❌ Truncated bytes.  ❌ Data displayed as mojibake.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Accented char displayed correctly, but entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed as mojibake, entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3.
* **Test 13:** 🟡 Accented characters displayed correctly, emoji converted to question mark.
* **Test 14:** Could not figure out how to configure QRZ lookups.

Exports:
* ADIF Export: encoded as ISO-8859-1, with field counts in bytes, one space between fields, CRLF between records. "Mojibake" preserved on export.

This app seems to:

* Use ISO-8859-1 or Win-1252 internally
* Count ADIF field in bytes
* Handle fields with data beyond length (undercount)
* Correctly limit UI input to ISO-8859-1


---

### [World Radio League](https://www.worldradioleague.com/)

**Version:** N/A

**Tested:** 2025-09-27 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with �.
* **Test 2:** 🟡 Dropped fields. ❌ Imported extra chars. ✅ Data displayed correctly.
* **Test 3:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 4:** 🟡 Dropped fields. ❌ Imported extra chars. ✅ Data displayed correctly.
* **Test 5:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 6:** 🟡 Dropped fields. ❌ Imported extra chars. ✅ Data displayed correctly.
* **Test 7:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
* **Test 8:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 9:** ✅ Imported QSO. ✅ Imported all bytes. 🟡 Data displayed correctly, entities not decoded.
* **Test 10:** ✅ Imported QSO. ✅ Imported all bytes. ❌ Data displayed with � and entities not decoded.
* **Test 11:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 12.
* **Test 12:** 🟡 Mixed results consistent with Test 1, 2 & 3. Same as Test 11.
* **Test 13:** ✅ Data displayed correctly.
* **Test 14:** ✅ Data displayed correctly.

Exports:
* ADIF Export: encoded as UTF-8, field counts in characters, one space between fields, two CRLF between records.

Notes: Import functionality has no options relevant to character encoding.

This app seems to:

* Use Unicode internally
* Count ADIF field in characters
* Handle fields with data beyond length (undercount)
* Fail to handle fields with length past data (overcount), dropping fields.
* Not transcode when importing or exporting
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI

---

