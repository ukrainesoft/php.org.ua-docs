---
navigation:
  - migration80.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration80.other-changes.md: Інші зміни »
  - index.md: PHP Manual
  - migration80.md: Міграція з PHP 7.4.x на PHP 8.0.x
title: 'Функціональність, оголошена застарілою в PHP 8.0.x'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Функціональність, оголошена застарілою в PHP 8.0.x

### Ядро PHP

-   Якщо за параметром за замовчуванням слід обов'язковий параметр, то значення за умовчанням не має сенсу. З PHP 8.0.0 такий порядок параметрів оголошений застарілим і може бути виправлений шляхом видалення значення за замовчуванням:
    
    ```php
    <?php
    function test($a ​​= [], $b) {} // До
    function test($a, $b) {} // Після
    ?>
    ```
    
    Одним із винятків із цього правила є параметри виду`Type $param = null`, де значення за умовчанням null робить тип явно обнулюваним. Це поки що дозволено, але натомість краще рекомендується використовувати явний тип nullable:
    
    ```php
    <?php
    function test(A $a = null, $b) {} // Як і раніше дозволено
    function test(?A $a, $b) {} // Рекомендується
    ?>
    ```
    
-   Виклик [get\_defined\_functions()](function.get-defined-functions.md)з явно заданим значенням\*\*`false`\*\*в`exclude_disabled` устарел и больше не имеет смысла . [get\_defined\_functions()](function.get-defined-functions.md)ніколи не повертатиме відключені функції.
    

### Enchant

-   [enchant\_broker\_set\_dict\_path()](function.enchant-broker-set-dict-path.md) і [enchant\_broker\_get\_dict\_path()](function.enchant-broker-get-dict-path.md) оголошені застарілими, оскільки вони недоступні ні libenchant < 1.5 ні libenchant-2.
    
-   [enchant\_dict\_add\_to\_personal()](function.enchant-dict-add-to-personal.md)оголошено застарілою; використовуйте замість неї[enchant\_dict\_add()](function.enchant-dict-add.md)
    
-   [enchant\_dict\_is\_in\_session()](function.enchant-dict-is-in-session.md)оголошено застарілою; використовуйте замість неї[enchant\_dict\_is\_added()](function.enchant-dict-is-added.md)
    
-   [enchant\_broker\_free()](function.enchant-broker-free.md) і [enchant\_broker\_free\_dict()](function.enchant-broker-free-dict.md)оголошені застарілими; замість неї застосовуйте до об'єкта функцію unset.
    
-   Константа\*\*`ENCHANT_MYSPELL`**и**`ENCHANT_ISPELL`\*\* оголошено застарілими.
    

### LibXML

[libxml\_disable\_entity\_loader()](function.libxml-disable-entity-loader.md) оголошено застарілою. Оскільки тепер використовується libxml 2.9.0, в якому завантаження зовнішніх об'єктів за замовчуванням вимкнуто, тому використання цієї функції більше не потрібне для захисту від XXE-атак, якщо не використовується (досі вразлива) **`LIBXML_NOENT`**. У цьому випадку рекомендується провести рефакторинг коду за допомогою [libxml\_set\_external\_entity\_loader()](function.libxml-set-external-entity-loader.md), щоб придушити завантаження зовнішніх сутностей.

### PGSQL / PDO PGSQL

-   Константа\*\*`PGSQL_LIBPQ_VERSION_STR`**тепер має те саме значення, що і**`PGSQL_LIBPQ_VERSION`\*\*і тому оголошено застарілою.
    
-   Псевдоніми функцій у модулі pgsql оголошені застарілими. Дивіться у списку, які функції слід використовувати замість них:
    
    -   **pg\_errormessage()** → [pg\_last\_error()](function.pg-last-error.md)
    -   **pg\_numrows()** → [pg\_num\_rows()](function.pg-num-rows.md)
    -   **pg\_numfields()** → [pg\_num\_fields()](function.pg-num-fields.md)
    -   **pg\_cmdtuples()** → [pg\_affected\_rows()](function.pg-affected-rows.md)
    -   **pg\_fieldname()** → [pg\_field\_name()](function.pg-field-name.md)
    -   **pg\_fieldsize()** → [pg\_field\_size()](function.pg-field-size.md)
    -   **pg\_fieldtype()** → [pg\_field\_type()](function.pg-field-type.md)
    -   **pg\_fieldnum()** → [pg\_field\_num()](function.pg-field-num.md)
    -   **pg\_result()** → [pg\_fetch\_result()](function.pg-fetch-result.md)
    -   **pg\_fieldprtlen()** → [pg\_field\_prtlen()](function.pg-field-prtlen.md)
    -   **pg\_fieldisnull()** → [pg\_field\_is\_null()](function.pg-field-is-null.md)
    -   **pg\_freeresult()** → [pg\_free\_result()](function.pg-free-result.md)
    -   **pg\_getlastoid()** → [pg\_last\_oid()](function.pg-last-oid.md)
    -   **pg\_locreate()** → [pg\_lo\_create()](function.pg-lo-create.md)
    -   **pg\_lounlink()** → [pg\_lo\_unlink()](function.pg-lo-unlink.md)
    -   **pg\_loopen()** → [pg\_lo\_open()](function.pg-lo-open.md)
    -   **pg\_loclose()** → [pg\_lo\_close()](function.pg-lo-close.md)
    -   **pg\_loread()** → [pg\_lo\_read()](function.pg-lo-read.md)
    -   **pg\_lowrite()** → [pg\_lo\_write()](function.pg-lo-write.md)
    -   **pg\_loreadall()** → [pg\_lo\_read\_all()](function.pg-lo-read-all.md)
    -   **pg\_loimport()** → [pg\_lo\_import()](function.pg-lo-import.md)
    -   **pg\_loexport()** → [pg\_lo\_export()](function.pg-lo-export.md)
    -   **pg\_setclientencoding()** → [pg\_set\_client\_encoding()](function.pg-set-client-encoding.md)
    -   **pg\_clientencoding()** -> [pg\_client\_encoding()](function.pg-client-encoding.md)

### Бібліотека стандартних функцій

-   Функції порівняння сортування, що повертають\*\*`true`**или**`false`\*\*тепер згенерує попередження про застарілі можливості, тому їх слід переписати, щоб вони повертали ціле число менше, рівне або більше нуля.
    
    ```php
    <?php
    // Замінити подібний код:
    usort($array, fn($a, $b) => $a > $b);
    // На цей:
    usort($array, fn($a, $b) => $a <=> $b);
    ?>
    ```
    

### Zip

-   Використання порожнього файлу в ZipArchive оголошено застарілим. Libzip 1.6.0 більше не працює з пустими zip-архівами. Існуюче обхідне рішення буде видалено у наступній версії.
    
-   Процедурний API Zip оголошено застарілим. Замість нього використовуйте[ZipArchive](class.ziparchive.md). Ітерацію по всіх записах можна виконати за допомогою[ZipArchive::statIndex()](ziparchive.statindex.md)та циклу[for](control-structures.for.md) :
    
    ```php
    <?php
    // Ітерація з використанням процедурного API
    assert(is_resource($zip));
    while ($entry = zip_read($zip)) {
        echo zip_entry_name($entry);
    }
    
    // ітерація з використанням об'єктно-орієнтованого API
    assert($zip instanceof ZipArchive);
    for ($i = 0; $entry = $zip->statIndex($i); $i++) {
        echo $entry['name'];
    }
    ?>
    ```
    

### Reflection

-   [ReflectionFunction::isDisabled()](reflectionfunction.isdisabled.md)оголошено застарілим, тому що більше неможливо створити[ReflectionFunction](class.reflectionfunction.md)для вимкненої функції. Цей метод тепер завжди повертає\*\*`false`\*\*
    
-   [ReflectionParameter::getClass()](reflectionparameter.getclass.md) [ReflectionParameter::isArray()](reflectionparameter.isarray.md) і [ReflectionParameter::isCallable()](reflectionparameter.iscallable.md)оголошено застарілими. Замість них слід використовувати[ReflectionParameter::getType()](reflectionparameter.gettype.md)та API[ReflectionType](class.reflectiontype.md)
