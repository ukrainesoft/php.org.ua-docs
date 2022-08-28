Функціонал, оголошений застарілим у PHP 7.3.x

-   [« Изменения, ломающие обратную совместимость](migration73.incompatible.html)
    
-   [Прочие изменения »](migration73.other-changes.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.2.x на PHP 7.3.x](migration73.html)
    
-   Функціонал, оголошений застарілим у PHP 7.3.x
    

## Функціонал, оголошений застарілим у PHP 7.3.x

### Ядро PHP

#### Нечутливі до регістру константи

Оголошення реєстронезалежних констант оголошено застарілим. Передача **`true`** як третій параметр функції [define()](function.define.html) тепер згенерує попередження про застарілі можливості. Використання нечутливих до регістру констант у разі, коли вони відрізняються від оголошення, також застаріло.

#### Використання assert() усередині просторів імен

Оголошення функції з ім'ям `assert()` усередині простору імен оголошено застарілим. Функція [assert()](function.assert.html) схильна до спеціальної обробки двигуном, що може призвести до неузгодженої поведінки щодо функції в просторі імен з тим же ім'ям.

#### Пошук рядків для нестрокового параметра needle

Передача нестрокового параметра needle у рядкові функції пошуку оголошено застарілим. У майбутньому цей параметр інтерпретуватиметься як рядок, а не як точка коду ASCII. Залежно від передбачуваної поведінки необхідно або явно привести параметр до рядка, або здійснити явний виклик [chr()](function.chr.html). Торкнулися такі функції:

-   [strpos()](function.strpos.html)
-   [strrpos()](function.strrpos.html)
-   [stripos()](function.stripos.html)
-   [strripos()](function.strripos.html)
-   [strstr()](function.strstr.html)
-   [strchr()](function.strchr.html)
-   [strrchr()](function.strrchr.html)
-   [stristr()](function.stristr.html)

#### Зміни у видаленні тегів

Функція [fgetss()](function.fgetss.html) і [фильтр потока string.strip\_tags](filters.string.html) оголошено застарілим. Це також впливає на метод [SplFileObject::fgetss()](splfileobject.fgetss.html) та на функцію [gzgetss()](function.gzgetss.html)

### Фільтрування даних

Явне використання констант **`FILTER_FLAG_SCHEME_REQUIRED`** і **`FILTER_FLAG_HOST_REQUIRED`** тепер оголошено застарілим; так чи інакше, вони мають на увазі використання **`FILTER_VALIDATE_URL`**

### Обробка зображень та GD

Функція [image2wbmp()](function.image2wbmp.html) оголошено застарілою.

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

Налаштування ini-файлу [pdo\_odbc.db2\_instance\_name](ref.pdo-odbc.html#ini.pdo-odbc.db2-instance-name) офіційно оголошено застарілим. Опція застаріла у документації, починаючи з PHP 5.1.1.