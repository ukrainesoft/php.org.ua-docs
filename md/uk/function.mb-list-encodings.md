- [«mb_language](function.mb-language.md)
- [mb_ord »](function.mb-ord.md)

- [PHP Manual](index.md)
- [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
- Повертає масив усіх підтримуваних кодувань

#mb_list_encodings

(PHP 5, PHP 7, PHP 8)

mb_list_encodings — Повертає масив усіх підтримуваних кодувань

### Опис

**mb_list_encodings**(): array

Повертає масив, що містить всі кодування, що підтримуються.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексний масив.

### Помилки

Ця функція не породжує жодних помилок.

### Приклади

**Приклад #1 Приклад використання **mb_list_encodings()****

` <?phpprint_r(mb_list_encodings());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => pass
[1] => auto
[2] => wchar
[3] => byte2be
[4] => byte2le
[5] => byte4be
[6] => byte4le
[7] => BASE64
[8] => UUENCODE
[9] => HTML-ENTITIES
[10] => Quoted-Printable
[11] => 7bit
[12] => 8bit
[13] => UCS-4
[14] => UCS-4BE
[15] => UCS-4LE
[16] => UCS-2
[17] => UCS-2BE
[18] => UCS-2LE
[19] => UTF-32
[20] => UTF-32BE
[21] => UTF-32LE
[22] => UTF-16
[23] => UTF-16BE
[24] => UTF-16LE
[25] => UTF-8
[26] => UTF-7
[27] => UTF7-IMAP
[28] => ASCII
[29] => EUC-JP
[30] => SJIS
[31] => eucJP-win
[32] => SJIS-win
[33] => JIS
[34] => ISO-2022-JP
[35] => Windows-1252
[36] => ISO-8859-1
[37] => ISO-8859-2
[38] => ISO-8859-3
[39] => ISO-8859-4
[40] => ISO-8859-5
[41] => ISO-8859-6
[42] => ISO-8859-7
[43] => ISO-8859-8
[44] => ISO-8859-9
[45] => ISO-8859-10
[46] => ISO-8859-13
[47] => ISO-8859-14
[48] => ISO-8859-15
[49] => EUC-CN
[50] => CP936
[51] => HZ
[52] => EUC-TW
[53] => BIG-5
[54] => EUC-KR
[55] => UHC
[56] => ISO-2022-KR
[57] => Windows-1251
[58] => CP866
[59] => KOI8-R
)

### Дивіться також

- [mb_encoding_aliases()](function.mb-encoding-aliases.md) -
Отримує псевдоніми відомого типу кодування
