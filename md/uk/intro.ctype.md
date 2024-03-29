---
navigation:
  - book.ctype.md: « Ctype
  - ctype.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.ctype.md: Ctype
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

Функції, представлені цим модулем, дозволяють перевірити належність символу або рядка певному класу символів, беручи до уваги поточні регіональні установки (дивіться також функцію [setlocale()](function.setlocale.md)

Будучи викликаними з цілим аргументом, ці функції поводяться точно так, як їх C-еквіваленти в мові C (з ctype.h). Це означає, що якщо передається ціле значення менше 256, функції перевіряють, чи це значення ASCII відповідає зазначеному класу символів (цифри знаходяться в діапазоні 0x30-0x39). Якщо число знаходиться в межах від -128 до -1 включно, то його значення буде додано 256 і порівняння буде проводитися з використанням результату додавання.

**Увага**

Починаючи з PHP 8.1.0, передача нерядкових аргументів застаріла. У майбутньому аргумент замість ASCII-коду інтерпретуватиметься як рядок. Залежно від передбачуваної поведінки аргумент або перетворюють у рядок (string), або викликають функцію [chr()](function.chr.md)

Якщо аргументом виступає рядок, то функції перевірятимуть кожен символ у цьому рядку і повернуть **`true`** тільки якщо кожен символ відповідає потрібній умові. При виклику з порожнім рядком результатом завжди буде **`false`**

При передачі інших типів (крім цілого чи рядка) функції відразу ж повертають **`false`**

Слід зазначити, що ці функції завжди кращі, ніж використання регулярних виразів і навіть деяких еквівалентних функцій `"str_*"`и`"is_*"`. Це з тим, що ctype використовує рідну бібліотеку З, отже, працюють значно швидше.

> **Зауваження** :
> 
> Ці функції не мають жодного відношення до Python-бібліотеки "ctypes". Назва модуля є скороченням імені заголовного файлу C ctype.h, в якому визначено еквіваленти C.
> 
> Модуль також був створений раніше "ctypes" в Python, тому будь-яка плутанина, пов'язана з цими назвами, навряд чи є помилкою з боку розробників модуля.
