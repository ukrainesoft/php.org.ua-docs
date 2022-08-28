Функціональність, оголошена застарілою в PHP 8.0.x

-   [« Изменения, ломающие обратную совместимость](migration80.incompatible.html)
    
-   [Другие изменения »](migration80.other-changes.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.4.x на PHP 8.0.x](migration80.html)
    
-   Функціональність, оголошена застарілою в PHP 8.0.x
    

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
    
-   Виклик [get\_defined\_functions()](function.get-defined-functions.html) з явно заданим значенням **`false`** в `exclude_disabled` застарів і більше не має сенсу . [get\_defined\_functions()](function.get-defined-functions.html) ніколи не повертатиме відключені функції.
    

### Enchant

-   [enchant\_broker\_set\_dict\_path()](function.enchant-broker-set-dict-path.html) і [enchant\_broker\_get\_dict\_path()](function.enchant-broker-get-dict-path.html) оголошені застарілими, оскільки вони недоступні ні libenchant < 1.5 ні libenchant-2.
    
-   [enchant\_dict\_add\_to\_personal()](function.enchant-dict-add-to-personal.html) оголошено застарілою; використовуйте замість неї [enchant\_dict\_add()](function.enchant-dict-add.html)
    
-   [enchant\_dict\_is\_in\_session()](function.enchant-dict-is-in-session.html) оголошено застарілою; використовуйте замість неї [enchant\_dict\_is\_added()](function.enchant-dict-is-added.html)
    
-   [enchant\_broker\_free()](function.enchant-broker-free.html) і [enchant\_broker\_free\_dict()](function.enchant-broker-free-dict.html) оголошені застарілими; замість неї застосовуйте до об'єкта функцію unset.
    
-   Константа **`ENCHANT_MYSPELL`** і **`ENCHANT_ISPELL`** оголошено застарілими.
    

### LibXML

[libxml\_disable\_entity\_loader()](function.libxml-disable-entity-loader.html) оголошено застарілою. Оскільки тепер використовується libxml 2.9.0, в якому завантаження зовнішніх об'єктів за замовчуванням вимкнуто, тому використання цієї функції більше не потрібне для захисту від XXE-атак, якщо не використовується (досі вразлива) **`LIBXML_NOENT`**. У цьому випадку рекомендується провести рефакторинг коду за допомогою [libxml\_set\_external\_entity\_loader()](function.libxml-set-external-entity-loader.html), щоб придушити завантаження зовнішніх сутностей.

### PGSQL / PDO PGSQL

-   Константа **`PGSQL_LIBPQ_VERSION_STR`** тепер має те саме значення, що і **`PGSQL_LIBPQ_VERSION`** і тому оголошено застарілою.
    
-   Псевдоніми функцій у модулі pgsql оголошені застарілими. Дивіться у списку, які функції слід використовувати замість них:
    
    -   **пгerrormessage()** [pg\_last\_error()](function.pg-last-error.html)
    -   **пгnumrows()** [pg\_num\_rows()](function.pg-num-rows.html)
    -   **пгnumfields()** [pg\_num\_fields()](function.pg-num-fields.html)
    -   **пгcmdtuples()** [pg\_affected\_rows()](function.pg-affected-rows.html)
    -   **пгfieldname()** [pg\_field\_name()](function.pg-field-name.html)
    -   **пгfieldsize()** [pg\_field\_size()](function.pg-field-size.html)
    -   **пгfieldtype()** [pg\_field\_type()](function.pg-field-type.html)
    -   **пгfieldnum()** [pg\_field\_num()](function.pg-field-num.html)
    -   **пгresult()** [pg\_fetch\_result()](function.pg-fetch-result.html)
    -   **пгfieldprtlen()** [pg\_field\_prtlen()](function.pg-field-prtlen.html)
    -   **пгfieldisnull()** [pg\_field\_is\_null()](function.pg-field-is-null.html)
    -   **пгfreeresult()** [pg\_free\_result()](function.pg-free-result.html)
    -   **пгgetlastoid()** [pg\_last\_oid()](function.pg-last-oid.html)
    -   **пгlocreate()** [pg\_lo\_create()](function.pg-lo-create.html)
    -   **пгlounlink()** [pg\_lo\_unlink()](function.pg-lo-unlink.html)
    -   **пгloopen()** [pg\_lo\_open()](function.pg-lo-open.html)
    -   **пгloclose()** [pg\_lo\_close()](function.pg-lo-close.html)
    -   **пгloread()** [pg\_lo\_read()](function.pg-lo-read.html)
    -   **пгlowrite()** [pg\_lo\_write()](function.pg-lo-write.html)
    -   **пгloreadall()** [pg\_lo\_read\_all()](function.pg-lo-read-all.html)
    -   **пгloimport()** [pg\_lo\_import()](function.pg-lo-import.html)
    -   **пгloexport()** [pg\_lo\_export()](function.pg-lo-export.html)
    -   **пгsetclientencoding()** [pg\_set\_client\_encoding()](function.pg-set-client-encoding.html)
    -   **пгclientencoding()** -> [pg\_client\_encoding()](function.pg-client-encoding.html)

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
    
-   Процедурний API Zip оголошено застарілим. Замість нього використовуйте [ZipArchive](class.ziparchive.html). Ітерацію по всіх записах можна виконати за допомогою [ZipArchive::statIndex()](ziparchive.statindex.html) та циклу [for](control-structures.for.html)
    
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

-   [ReflectionFunction::isDisabled()](reflectionfunction.isdisabled.html) оголошено застарілим, тому що більше неможливо створити [ReflectionFunction](class.reflectionfunction.html) для вимкненої функції. Цей метод тепер завжди повертає **`false`**
    
-   [ReflectionParameter::getClass()](reflectionparameter.getclass.html) [ReflectionParameter::isArray()](reflectionparameter.isarray.html) і [ReflectionParameter::isCallable()](reflectionparameter.iscallable.html) оголошено застарілими. Замість них слід використовувати [ReflectionParameter::getType()](reflectionparameter.gettype.html) та API [ReflectionType](class.reflectiontype.html)