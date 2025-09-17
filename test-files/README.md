# Explanation of the tests

## 1: 8859.adi

Check for support of importing ISO-8859-1 characters.

A single QSO with `name` "Juán Muñoz" and `qth` "El Cañón", encoded as ISO-8859-1.

To work as expected, the app should display the name and QTH correctly.

If the app uses Unicode internally, and always reads files as UTF-8, then
it will display Something like "Ju�n Mu�oz".

If the app does not support Unicode, it will likely pass this test.

## 2: UTF-bytes.adi

Check for support of importing UTF-8 characters with byte counts.

A single QSO with `name` "Juán Muñoz" and `qth` "El Cañón", encoded as UTF-8 with field counts in bytes.

If the app does not support Unicode, it will display something like "JuÃ¡n MuÃ±oz".

If the app supports Unicode, and uses byte counts,it will likely pass this test.

If the app supports Unicode, and uses character counts, it might include an extra CRLF in the field data, or it might handle it gracefuly.

## 3: UTF-chars.adi

Check for support of importing UTF-8 characters with character counts.

A single QSO with `name` "Juán Muñoz" and `qth` "El Cañón", encoded as UTF-8 with field counts in characters.

If the app does not support Unicode, it will display something like "JuÃ¡n MuÃ±oz".

If the app supports Unicode, and uses character counts, it will likely pass this test.

If the app supports Unicode, and uses byte counts, it will likely show a shortened version of the values, missing the last two letters, like "Juán Muñ" or "El Cañ".

## 4: UTF-bytes-tight.adi

Check for support of importing UTF-8 characters with byte counts and "tight" fields.

A single QSO with `name` "Juán Muñoz" and `qth` "1️⃣2️⃣3️⃣4️⃣5️⃣", encoded as UTF-8 with field counts in bytes. The "tight" refers to not having extra spaces or line breaks between fields.

If the app does not support Unicode, it will display something like "JuÃ¡n MuÃ±oz" or just mojibake instead of the emoji.

If the app supports Unicode, and uses byte counts, it will likely show a shortened version of the values, missing the last two letters, like "Juán Muñ" or "1️⃣2️⃣3️⃣".

If the app supports Unicode, and uses character counts, it might skip fields like `call` and `freq` resulting in an invalid QSO.

If the app supports Unicode and imports this correctly, it might be doing additional field parsing and boundary detection beyond field counts.

## 5: UTF-chars-tight.adi

Check for support of importing UTF-8 characters with character counts and "tight" fields.

A single QSO with `name` "Juán Muñoz" and `qth` "1️⃣2️⃣3️⃣4️⃣5️⃣", encoded as UTF-8 with field counts in characters. The "tight" refers to not having extra spaces or line breaks between fields.

If the app does not support Unicode, it will likely skip fields like `call` and `freq` resulting in an invalid QSO.

If the app does not support Unicode, but displays something like "JuÃ¡n MuÃ±oz" or "El CaÃ±Ã³n", it might be doing additional field parsing and boundary detection beyond field counts.

If the app supports Unicode, and uses character counts, it will likely pass this test.

# 6: UTF-extended-bytes.adi

Check for support of importing UTF-8 characters beyond Latin 1, with byte counts.

A single QSO with `name` "Korean example: 이건 예시예요.", encoded as UTF-8 with field counts in bytes.

If the app supports Unicode, and uses byte counts, it will likely pass this test.

If the app supports Unicode, and uses character counts, it might display a truncated name, without a period "." at the end.

If the app does not support Unicode, it will show something like "Korean example: ì�´ê±´ ì˜ˆì‹œì˜ˆìš”."

# 7: UTF-extended-chars.adi

Check for support of importing UTF-8 characters beyond Latin 1, with character counts.

A single QSO with `name` "Korean example: 이건 예시예요.", encoded as UTF-8 with field counts in characters.

If the app supports Unicode, and uses character counts, it will likely pass this test.

If the app supports Unicode, and uses byte counts, it might skip fields like `qso_date` resulting in an invalid QSO.

If the app does not support Unicode, it will show a truncated version with mojibake like "Korean example: ì�´ê±´ ì˜"

# 8: 8859-entities.adi

Check for support of importing ISO-8859-1 characters with both HTML entities and ISO-8859-1 encoded characters.

A single QSO with `name` "Juán Mu&ntilde;oz" and `qth` "El Cañ&#243;n", encoded as ISO-8859-1 with some characters encoded as HTML entities.

If the app supports HTML entities, it will likely show the values with the HTML entities replaced with the actual characters: "Juán Muñoz" and "El Cañón".

If the app does not support HTML entities, it will likely show the values with the "&...;" entities and the rest of the characters behaving as they to in Test 1.

# 9: UTF-entities.adi

Check for support of importing UTF-8 characters with both HTML entities and UTF-8 encoded characters.

A single QSO with `name` "Juán Mu&ntilde;oz" and `qth` "El Cañ&#243;n", encoded as UTF-8 with some characters encoded as HTML entities.

If the app supports HTML entities, it will likely show the values with the HTML entities replaced with the actual characters: "Juán Muñoz" and "El Cañón".

If the app does not support HTML entities, it will likely show the values with the "&...;" entities and the rest of the characters behaving as they to in Test 2.

# 10: UTF-extended-entities.adi

Check for support of importing UTF-8 characters beyond Latin 1 encoded as HTML entities, along with accented characters encoded as ISO-8859-1.

A single QSO with `name` "Korean example: &#xC774;&#xAC83;&#xC740;&#x20;&#xC608;&#xC2DC;&#xC785;&#xB2C8;&#xB2E4;" and `qth` "El Cañ&#243;n", encoded as ISO-8859-1, with counts in bytes.

If the app supports Unicode, HTML entities, and default encoding of ISO-8859-1, it will likely show the values with the HTML entities replaced with the actual characters: "Korean example: 한글 예제" and "El Cañón".

If the app does not support HTML entities, it will likely show the values with the "&...;" entities and the rest of the characters behaving as they to in Test 6.

If the supports Unicode but opens the file as UTF-8, it will show an invalid character in "El Ca�&#243;n" or "El Cañón".

# 11: mixed-chars.adi

Check for support of importing mixed encodings, with character counts.

This test includes multiple QSOs, all with `name` "Juán Muñoz" and `qth` "El Cañón", but with different encodings and counts.

- `call` "K1ISO" with ISO-8859-1 characters with byte counts
- `call` "K2UTF" with UTF-8 characters with character counts
- `call` "K3UTF" with UTF-8 characters with byte counts
- `call` "K4MIX" with mixed UTF-8 and ISO-8859-1 on different fields, with character counts

There's no easy way to describe the expected results. Apps are not expected to work correctly for all four QSOs at the same time.

# 12: mixed-chars-2.adi

Check for support of importing mixed encodings, with character counts.

This test is similar to Test 11, but instead of the first QSO having ISO-8859-1 characters
it has UTF-8 characters, in order to test if the app is doing encoding detection.

- `call` "K1UTF" with UTF-8 characters with character counts
- `call` "K2ISO" with ISO-8859-1 characters with byte counts
- `call` "K3UTF" with UTF-8 characters with byte counts
- `call` "K4MIX" with mixed UTF-8 and ISO-8859-1 on different fields, with character counts

If the app is doing encoding detection based on the first set of extended characters found, it will show results different from Test 11. Call "K1ISO" from Test 11 and "K1UTF" from Test 12 will display the correct name, or both will have different variations of mojibake.

If the app always opens files with the same encoding, then call "K1ISO" from Test 11 will show correctly and "K2ISO" from Test 12 will show mojibake, or vice versa.

# 13: enter-data.txt

This is not an ADIF file but a text file with instructions.

It asks the user to use the app's interface to enter a new QSO with a name that includes Latin 1 and extended Unicode characters.

If the app supports Unicode, it will show the full value entered.

If the app does not support Unicode, it will most likely not include the emoji, but correctly handle the accented letters.

If the app does not support Unicode and does not support Latin 1, it will most likely just show a truncated value.

# 14: qrz-lookups.txt

This is not an ADIF file but a text file with instructions.

It asks the user to use the app's interface to use the QRZ.com API to lookup for contact detals.

The file includes callsigns known to have accented characters correctly or incorrectly encoded.

There's no easy way to describe the expected results. Apps are not expected to work correctly for all cases.
