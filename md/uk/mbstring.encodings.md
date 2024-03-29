---
navigation:
  - mbstring.constants.md: « Зумовлені константи
  - mbstring.ja-basic.md: Основи японських багатобайтних кодувань
  - index.md: PHP Manual
  - book.mbstring.md: Багатобайтові рядки
title: Короткий огляд підтримуваних кодувань
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Короткий огляд підтримуваних кодувань

**Список підтримуваних кодувань**

| Название в реестре кодировок IANA | Лежащий в основе набор символов | Опис | Дополнительная информация |
| --- | --- | --- | --- |
| ISO-10646-UCS-4 | ISO 10646 | Універсальний набір символів з 31 бітом для коду символу, стандартизований ISO/IEC 10646 як UCS-4. Встановлено синхронізацію зі стандартом Юнікод. | Якщо ця назва використовується у засобах перетворення кодувань, конвертер спробує визначити порядок розташування байтів за BOM (мітка порядку байтів). |
| ISO-10646-UCS-4 | UCS-4 | Дивіться вище. | В отличие от`UCS-4`, Рядки завжди приймаються закодованими в прямому порядку розташування байтів. |
| ISO-10646-UCS-4 | UCS-4 | Дивіться вище. | В отличие от`UCS-4`, Рядки завжди приймаються закодованими в зворотному порядку розташування байтів. |
| ISO-10646-UCS-2 | UCS-2 | Універсальний набір символів з 16 бітом для коду символу, стандартизований ISO/IEC 10646 як UCS-2. Встановлено синхронізацію зі стандартом Юнікод. | Якщо ця назва використовується у засобах перетворення кодувань, конвертер спробує визначити порядок розташування байтів за BOM (мітка порядку байтів). |
| ISO-10646-UCS-2 | UCS-2 | Дивіться вище. | В отличие от`UCS-2`, Рядки завжди приймаються закодованими в прямому порядку розташування байтів. |
| ISO-10646-UCS-2 | UCS-2 | Дивіться вище. | В отличие от`UCS-2`, Рядки завжди приймаються закодованими в зворотному порядку розташування байтів. |
| UTF-32 | Юнікод | Формат перетворення Юнікоду з 32-бітною шириною символу, кодовий простір якого відповідає стандарту кодової таблиці Юнікоду. Ця схема кодування не ідентична UCS-4, оскільки кодовий простір Юнікод обмежено 21-м бітом. | Якщо ця назва використовується у засобах перетворення кодувань, конвертер спробує визначити порядок розташування байтів за BOM (мітка порядку байтів). |
| UTF-32BE | Юнікод | Дивіться вище | В отличие от`UTF-32`, Рядки завжди приймаються закодованими в прямому порядку розташування байтів. |
| UTF-32LE | Юнікод | Дивіться вище | В отличие от`UTF-32`, Рядки завжди приймаються закодованими в зворотному порядку розташування байтів. |
| UTF-16 | Юнікод | Формат перетворення Юнікоду з 32-бітною шириною коду символу. Специфікація UTF-16 відрізняється від UCS-2 через те, що починаючи з Юнікод 2.0 було впроваджено механізм заміщення символів і тепер UTF-16 посилається на 21-бітовий кодовий простір. | Якщо ця назва використовується у засобах перетворення кодувань, конвертер спробує визначити порядок розташування байтів за BOM (мітка порядку байтів). |
| UTF-16BE | Юнікод | Дивіться вище. | В отличие от`UTF-16`, Рядки завжди приймаються закодованими в прямому порядку розташування байтів. |
| UTF-16LE | Юнікод | Дивіться вище. | В отличие от`UTF-16`, Рядки завжди приймаються закодованими в зворотному порядку розташування байтів. |
| UTF-8 | Юнікод / ​​UCS | Формат перетворення Юнікоду з 32-бітною шириною коду символу. | ні |
| UTF-7 | Юнікод | Безпечний для поштових програм та рішень формат перетворення Юнікоду, визначений у специфікації [» RFC2152](http://www.faqs.org/rfcs/rfc2152) | ні |
| (ні) | Юнікод | Різновид UTF-7, спеціально розроблений для використання в [» протоколі IMAP](http://www.faqs.org/rfcs/rfc3501) | ні |
| US-ASCII (переважне MIME-ім'я) / iso-ir-6 / ANSI\_X3.4-1986 / ISO\_646.irv:1991 / ASCII / ISO646-US / us / IBM367 / CP367 / csASCII | ASCII / ISO 646 | ASCII (American Standard Code for Information Interchange – американський стандартний код для обміну інформацією) – широко використовується 7-бітове кодування. Також стандартизований як міжнародний стандарт ISO 646. | (ні) |
| EUC-JP (переважне MIME-ім'я) / Extended\_UNIX\_Code\_Packed\_Format\_for\_Japanese / csEUCPkdFmtJapanese | Об'єднання US-ASCII / JIS X0201:1997 (частина hankaku kana) / JIS X0208:1990 / JIS X0212:1990 | Як видно з назви, це кодування використовується в основному в Unix системах або подібних до них. Вихідна схема кодування Extended UNIX Code лягла основою стандарту ISO 2022. | Набір символів, на який посилається EUC-JP, відрізняється від набору для IBM932/CP932, які використовуються в OS/2® та Microsoft® Windows®. Для забезпечення взаємодії між цими платформами використовуйте кодування EUCJP-WIN. |
| Shift\_JIS (переважне MIME-ім'я) / MS\_Kanji / csShift\_JIS | Об'єднання JIS X0201:1997 / JIS X0208:1997 | Shift\_JIS був розроблений на початку 80-х, коли Японські текстові процесори для рядових користувачів лише виходили на ринок, щоб зберегти сумісність із схемою кодування JIS X 0201:1976. Відповідно до визначення IANA, кодова таблиця Shift\_JIS дещо відрізняється від IBM932/CP932. Тим не менш, назви "SJIS" / "Shift\_JIS" помилково використовуються для звернення до цих кодових таблиць. | Для кодової таблиці CP932 використовуйте кодування SJIS-WIN. |
| (none) | Об'єднання JIS X0201:1997 / JIS X0208:1997 / IBM розширення / NEC розширення | Незважаючи на те, що це "кодування" використовує ту ж схему кодування, що і EUC-JP, набори символів, що лежать у їх основі, різні. Таким чином, деякі коди посилаються на символи, відмінні від EUC-JP. | ні |
| Windows-31J / csWindows31J | Об'єднання JIS X0201:1997 / JIS X0208:1997 / IBM розширення / NEC розширення | Незважаючи на те, що це "кодування" використовує ту ж схему кодування, що і Shift\_JIS, набори символів, що лежить в їхній основі, різні. Таким чином, деякі коди посилаються на відмінні від Shift\_JIS символи. | (ні) |
| ISO-2022-JP (переважне MIME-ім'я) / csISO2022JP | US-ASCII / JIS X0201:1976 / JIS X0208:1978 / JIS X0208:1983 | [» RFC1468](http://www.faqs.org/rfcs/rfc1468) | (ні) |
| JIS |  |  |  |
| ISO-8859-1 |  |  |  |
| ISO-8859-2 |  |  |  |
| ISO-8859-3 |  |  |  |
| ISO-8859-4 |  |  |  |
| ISO-8859-5 |  |  |  |
| ISO-8859-6 |  |  |  |
| ISO-8859-7 |  |  |  |
| ISO-8859-8 |  |  |  |
| ISO-8859-9 |  |  |  |
| ISO-8859-10 |  |  |  |
| ISO-8859-13 |  |  |  |
| ISO-8859-14 |  |  |  |
| ISO-8859-15 |  |  |  |
| ISO-8859-16 |  |  |  |
| byte2be |  |  |  |
| byte2le |  |  |  |
| byte4be |  |  |  |
| byte4le |  |  |  |
| BASE64 |  |  |  |
| HTML-ENTITIES |  |  |  |
| 7bit |  |  |  |
| 8bit |  |  |  |
| EUC-CN |  |  |  |
| CP936 |  |  |  |
| HZ |  |  |  |
| EUC-TW |  |  |  |
| CP950 |  |  |  |
| BIG-5 |  |  |  |
| EUC-KR |  |  |  |
| UHC (CP949) |  |  |  |
| ISO-2022-KR |  |  |  |
| Windows-1251 (CP1251) |  |  |  |
| Windows-1252 (CP1252) |  |  |  |
| CP866 (IBM866) |  |  |  |
| KOI8-R |  |  |  |
| KOI8-U |  |  |  |
