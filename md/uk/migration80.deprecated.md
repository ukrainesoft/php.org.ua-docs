---
navigation:
  - migration80.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration80.other-changes.md: Другие изменения »
  - index.md: PHP Manual
  - migration80.md: Миграция с PHP 7.4.x на PHP 8.0.x
title: 'Функціональність, оголошена застарілою в PHP 8.0.x'
---
## Функціональність, оголошена застарілою в PHP 8.0.x

### Ядро PHP

-   Якщо за параметром за замовчуванням слід обов'язковий параметр, то значення за умовчанням не має сенсу. З PHP 8.0.0 такий порядок параметрів оголошений застарілим і може бути виправлений шляхом видалення значення за замовчуванням:
    
    ```php
    <?php
    function test($a = [], $b) {} // До
    function test($a, $b) {}      // После
    ?>
    ```
    
    Одним із винятків із цього правила є параметри виду `Type $param = null`, де значення за умовчанням null робить тип явно обнулюваним. Це поки що дозволено, але натомість краще рекомендується використовувати явний тип nullable:
    
    ```php
    <?php
    function test(A $a = null, $b) {} // По-прежнему разрешено
    function test(?A $a, $b) {}       // Рекомендуется
    ?>
    ```
    
-   Виклик [getdefinedfunctions()](function.get-defined-functions.md) з явно заданим значенням **`false`** в `exclude_disabled` застарів і більше не має сенсу . [getdefinedfunctions()](function.get-defined-functions.md) ніколи не повертатиме відключені функції.
    

### Enchant

-   [enchantbrokersetdictpath()](function.enchant-broker-set-dict-path.md) і [enchantbrokergetdictpath()](function.enchant-broker-get-dict-path.md) оголошені застарілими, оскільки вони недоступні ні libenchant < 1.5 ні libenchant-2.
    
-   [enchantdictaddтоpersonal()](function.enchant-dict-add-to-personal.md) оголошено застарілою; використовуйте замість неї [enchantdictadd()](function.enchant-dict-add.md)
    
-   [enchantdictісінsession()](function.enchant-dict-is-in-session.md) оголошено застарілою; використовуйте замість неї [enchantdictісadded()](function.enchant-dict-is-added.md)
    
-   [enchantbrokerfree()](function.enchant-broker-free.md) і [enchantbrokerfreedict()](function.enchant-broker-free-dict.md) оголошені застарілими; замість неї застосовуйте до об'єкта функцію unset.
    
-   Константа **`ENCHANT_MYSPELL`** і **`ENCHANT_ISPELL`** оголошено застарілими.
    

### LibXML

[libxmldisableentityloader()](function.libxml-disable-entity-loader.md) оголошено застарілою. Оскільки тепер використовується libxml 2.9.0, в якому завантаження зовнішніх об'єктів за замовчуванням вимкнуто, тому використання цієї функції більше не потрібне для захисту від XXE-атак, якщо не використовується (досі вразлива) **`LIBXML_NOENT`**. У цьому випадку рекомендується провести рефакторинг коду за допомогою [libxmlsetexternalentityloader()](function.libxml-set-external-entity-loader.md), щоб придушити завантаження зовнішніх сутностей.

### PGSQL / PDO PGSQL

-   Константа **`PGSQL_LIBPQ_VERSION_STR`** тепер має те саме значення, що і **`PGSQL_LIBPQ_VERSION`** і тому оголошено застарілою.
    
-   Псевдоніми функцій у модулі pgsql оголошені застарілими. Дивіться у списку, які функції слід використовувати замість них:
    
    -   **пгerrormessage()** [пгlasterror()](function.pg-last-error.md)
    -   **пгnumrows()** [пгnumrows()](function.pg-num-rows.md)
    -   **пгnumfields()** [пгnumfields()](function.pg-num-fields.md)
    -   **пгcmdtuples()** [пгaffectedrows()](function.pg-affected-rows.md)
    -   **пгfieldname()** [пгfieldname()](function.pg-field-name.md)
    -   **пгfieldsize()** [пгfieldsize()](function.pg-field-size.md)
    -   **пгfieldtype()** [пгfieldtype()](function.pg-field-type.md)
    -   **пгfieldnum()** [пгfieldnum()](function.pg-field-num.md)
    -   **пгresult()** [пгfetchresult()](function.pg-fetch-result.md)
    -   **пгfieldprtlen()** [пгfieldprtlen()](function.pg-field-prtlen.md)
    -   **пгfieldisnull()** [пгfieldісnull()](function.pg-field-is-null.md)
    -   **пгfreeresult()** [пгfreeresult()](function.pg-free-result.md)
    -   **пгgetlastoid()** [пгlastoid()](function.pg-last-oid.md)
    -   **пгlocreate()** [пглоcreate()](function.pg-lo-create.md)
    -   **пгlounlink()** [пглоunlink()](function.pg-lo-unlink.md)
    -   **пгloopen()** [пглоopen()](function.pg-lo-open.md)
    -   **пгloclose()** [пглоclose()](function.pg-lo-close.md)
    -   **пгloread()** [пглоread()](function.pg-lo-read.md)
    -   **пгlowrite()** [пглоwrite()](function.pg-lo-write.md)
    -   **пгloreadall()** [пглоreadall()](function.pg-lo-read-all.md)
    -   **пгloimport()** [пглоimport()](function.pg-lo-import.md)
    -   **пгloexport()** [пглоexport()](function.pg-lo-export.md)
    -   **пгsetclientencoding()** [пгsetclientencoding()](function.pg-set-client-encoding.md)
    -   **пгclientencoding()** -> [пгclientencoding()](function.pg-client-encoding.md)

### Бібліотека стандартних функцій

-   Функції порівняння сортування, що повертають **`true`** або **`false`** тепер згенерує попередження про застарілі можливості, тому їх слід переписати, щоб вони повертали ціле число менше, рівне або більше нуля.
    
    ```php
    <?php
    // Заменить подобный код:
    usort($array, fn($a, $b) => $a > $b);
    // На этот:
    usort($array, fn($a, $b) => $a <=> $b);
    ?>
    ```
    

### Zip

-   Використання порожнього файлу в ZipArchive оголошено застарілим. Libzip 1.6.0 більше не працює з пустими zip-архівами. Існуюче обхідне рішення буде видалено у наступній версії.
    
-   Процедурний API Zip оголошено застарілим. Замість нього використовуйте [ZipArchive](class.ziparchive.md). Ітерацію по всіх записах можна виконати за допомогою [ZipArchive::statIndex()](ziparchive.statindex.md) та циклу [for](control-structures.for.md)
    
    ```php
    <?php
    // итерация с использованием процедурного API
    assert(is_resource($zip));
    while ($entry = zip_read($zip)) {
        echo zip_entry_name($entry);
    }
    
    // итерация с использованием объектно-ориентированного API
    assert($zip instanceof ZipArchive);
    for ($i = 0; $entry = $zip->statIndex($i); $i++) {
        echo $entry['name'];
    }
    ?>
    ```
    

### Reflection

-   [ReflectionFunction::isDisabled()](reflectionfunction.isdisabled.md) оголошено застарілим, тому що більше неможливо створити [ReflectionFunction](class.reflectionfunction.md) для вимкненої функції. Цей метод тепер завжди повертає **`false`**
    
-   [ReflectionParameter::getClass()](reflectionparameter.getclass.md) [ReflectionParameter::isArray()](reflectionparameter.isarray.md) і [ReflectionParameter::isCallable()](reflectionparameter.iscallable.md) оголошено застарілими. Замість них слід використовувати [ReflectionParameter::getType()](reflectionparameter.gettype.md) та API [ReflectionType](class.reflectiontype.md)
