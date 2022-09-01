---
navigation:
  - migration73.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration73.other-changes.html: Прочие изменения »
  - index.md: PHP Manual
  - migration73.md: Миграция с PHP 7.2.x на PHP 7.3.x
title: 'Функціонал, оголошений застарілим у PHP 7.3.x'
---
## Функціонал, оголошений застарілим у PHP 7.3.x

### Ядро PHP

#### Нечутливі до регістру константи

Оголошення реєстронезалежних констант оголошено застарілим. Передача **`true`** як третій параметр функції [define()](function.define.md) тепер згенерує попередження про застарілі можливості. Використання нечутливих до регістру констант у разі, коли вони відрізняються від оголошення, також застаріло.

#### Використання assert() усередині просторів імен

Оголошення функції з ім'ям `assert()` усередині простору імен оголошено застарілим. Функція [assert()](function.assert.md) схильна до спеціальної обробки двигуном, що може призвести до неузгодженої поведінки щодо функції в просторі імен з тим же ім'ям.

#### Пошук рядків для нестрокового параметра needle

Передача нестрокового параметра needle у рядкові функції пошуку оголошено застарілим. У майбутньому цей параметр інтерпретуватиметься як рядок, а не як точка коду ASCII. Залежно від передбачуваної поведінки необхідно або явно привести параметр до рядка, або здійснити явний виклик [chr()](function.chr.md). Торкнулися такі функції:

-   [strpos()](function.strpos.md)
-   [strrpos()](function.strrpos.md)
-   [stripos()](function.stripos.md)
-   [strripos()](function.strripos.md)
-   [strstr()](function.strstr.md)
-   [strchr()](function.strchr.md)
-   [strrchr()](function.strrchr.md)
-   [stristr()](function.stristr.md)

#### Зміни у видаленні тегів

Функція [fgetss()](function.fgetss.md) і [фильтр потока string.striptags](filters.string.md) оголошено застарілим. Це також впливає на метод [SplFileObject::fgetss()](splfileobject.fgetss.md) та на функцію [gzgetss()](function.gzgetss.md)

### Фільтрування даних

Явне використання констант **`FILTER_FLAG_SCHEME_REQUIRED`** і **`FILTER_FLAG_HOST_REQUIRED`** тепер оголошено застарілим; так чи інакше, вони мають на увазі використання **`FILTER_VALIDATE_URL`**

### Обробка зображень та GD

Функція [image2wbmp()](function.image2wbmp.md) оголошено застарілою.

### Функції інтернаціоналізації

Використання **`Normalizer::NONE`** викликає попередження про застарілу поведінку, якщо PHP не скомпільовано з ICU версії ≥ 56.

### Мультибайтові рядки

Наступні недокументовані псевдоніми `mbereg_*()` оголошено застарілими. Натомість використовуйте відповідні варіанти `mb_ereg_*()`

-   **mbregexencoding()**
-   **mbereg()**
-   **mberegi()**
-   **mberegreplace()**
-   **mberegireplace()**
-   **mbsplit()**
-   **mberegmatch()**
-   **mberegsearch()**
-   **mberegsearchpos()**
-   **mberegsearchregs()**
-   **mberegsearchinit()**
-   **mberegsearchgetregs()**
-   **mberegsearchgetpos()**
-   **mberegsearchsetpos()**

### Функції ODBC та DB2 (PDOODBC)

Налаштування ini-файлу [pdoodbc.db2instancename](ref.pdo-odbc.html#ini.pdo-odbc.db2-instance-name) офіційно оголошено застарілим. Опція застаріла у документації, починаючи з PHP 5.1.1.
