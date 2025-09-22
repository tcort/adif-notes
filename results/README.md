# Extended test results

Based on the files described in [test-files/README.md](test-files/README.md).

⁉️ Indicates unexpected findings.
🥳 Indicates unexpected positive findings.
😭 Indicate unexpected negative findings.


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
* Handle fields with data beyond length
* Handle fields with length shorter than data 🥳
* Not transcode ISO-8859-1 when importing
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI
* Mis-transcode lookup data, apparently treating UTF-8 source data as ISO-8859-1 and then trying to transcode that to UTF-8 😭



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
* ADIF Export: encoded as ISO-8859-1, with field counts in bytes, one space between fields, CRLF between records.

Notes: Import functionality has an option for "non-compliant ADIF", but it does not seem to make any difference in these results.

This app seems to:

* Use ISO-8859-1 or Win-1252 internally
* Count ADIF field in bytes
* Handle fields with data beyond length
* Not transcode UTF-8 when importing
* Not transcode HTML entities when importing
* Correctly limit UI input to ISO-8859-1
* Transcode lookup data 🥳, as 7-bit ASCII


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
* Handle fields with data beyond length
* Handle importing files with different encodings, autodetecting encoding and transcoding if necessary
* Seems to assume that files that have invalid UTF-8 sequences are encoded as ISO-8859-1
* Not transcode HTML entities when importing
* Correctly interpret lookup data as UTF-8


### [N1MM+](https://www.n1mm.com/)

**Version:** 1.0.10923

**Tested:** 2025-09-20 by KI2D

* **Test 1:** ✅ Imported QSO. ✅ Imported all bytes. ✅ Data displayed correctly.
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
* Not handle fields with length shorter than data
* Always imports as UTF-8 and always exports as transcodedISO-8859-1, with no autodetection.
* Not transcode HTML entities when importing
* Correctly accept Unicode input in the UI



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
* Transcode ISO-8859-1 using some different codepage. Accented `á` shows up as `б` (delta) and `ñ` shows up as `с`.
* Not transcode HTML entities when importing
* Remove UTF byte sequences on export, but preserve non-UTF byte sequences
* Correctly accept Unicode input in the UI


