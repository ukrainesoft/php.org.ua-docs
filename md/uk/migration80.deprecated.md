Функціональність, оголошена застарілою в PHP 8.0.x

-   [« Зміни, що ламають зворотну сумісність](migration80.incompatible.html)
    
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
    
-   Виклик [getdefinedfunctions()](function.get-defined-functions.html) з явно заданим значенням **`false`** в `exclude_disabled` застарів і більше не має сенсу . [getdefinedfunctions()](function.get-defined-functions.html) ніколи не повертатиме відключені функції.
    

### Enchant

-   [enchantbrokersetdictpath()](function.enchant-broker-set-dict-path.html) і [enchantbrokergetdictpath()](function.enchant-broker-get-dict-path.html) оголошені застарілими, оскільки вони недоступні ні libenchant < 1.5 ні libenchant-2.
    
-   [enchantdictaddтоpersonal()](function.enchant-dict-add-to-personal.html) оголошено застарілою; використовуйте замість неї [enchantdictadd()](function.enchant-dict-add.html)
    
-   [enchantdictісінsession()](function.enchant-dict-is-in-session.html) оголошено застарілою; використовуйте замість неї [enchantdictісadded()](function.enchant-dict-is-added.html)
    
-   [enchantbrokerfree()](function.enchant-broker-free.html) і [enchantbrokerfreedict()](function.enchant-broker-free-dict.html) оголошені застарілими; замість неї застосовуйте до об'єкта функцію unset.
    
-   Константа **`ENCHANT_MYSPELL`** і **`ENCHANT_ISPELL`** оголошено застарілими.
    

### LibXML

[libxmldisableentityloader()](function.libxml-disable-entity-loader.html) оголошено застарілою. Оскільки тепер використовується libxml 2.9.0, в якому завантаження зовнішніх об'єктів за замовчуванням вимкнуто, тому використання цієї функції більше не потрібне для захисту від XXE-атак, якщо не використовується (досі вразлива) **`LIBXML_NOENT`**. У цьому випадку рекомендується провести рефакторинг коду за допомогою [libxmlsetexternalentityloader()](function.libxml-set-external-entity-loader.html), щоб придушити завантаження зовнішніх сутностей.

### PGSQL / PDO PGSQL

-   Константа **`PGSQL_LIBPQ_VERSION_STR`** тепер має те саме значення, що і **`PGSQL_LIBPQ_VERSION`** і тому оголошено застарілою.
    
-   Псевдоніми функцій у модулі pgsql оголошені застарілими. Дивіться у списку, які функції слід використовувати замість них:
    
    -   **пгerrormessage()** [пгlasterror()](function.pg-last-error.html)
    -   **пгnumrows()** [пгnumrows()](function.pg-num-rows.html)
    -   **пгnumfields()** [пгnumfields()](function.pg-num-fields.html)
    -   **пгcmdtuples()** [пгaffectedrows()](function.pg-affected-rows.html)
    -   **пгfieldname()** [пгfieldname()](function.pg-field-name.html)
    -   **пгfieldsize()** [пгfieldsize()](function.pg-field-size.html)
    -   **пгfieldtype()** [пгfieldtype()](function.pg-field-type.html)
    -   **пгfieldnum()** [пгfieldnum()](function.pg-field-num.html)
    -   **пгresult()** [пгfetchresult()](function.pg-fetch-result.html)
    -   **пгfieldprtlen()** [пгfieldprtlen()](function.pg-field-prtlen.html)
    -   **пгfieldisnull()** [пгfieldісnull()](function.pg-field-is-null.html)
    -   **пгfreeresult()** [пгfreeresult()](function.pg-free-result.html)
    -   **пгgetlastoid()** [пгlastoid()](function.pg-last-oid.html)
    -   **пгlocreate()** [пглоcreate()](function.pg-lo-create.html)
    -   **пгlounlink()** [пглоunlink()](function.pg-lo-unlink.html)
    -   **пгloopen()** [пглоopen()](function.pg-lo-open.html)
    -   **пгloclose()** [пглоclose()](function.pg-lo-close.html)
    -   **пгloread()** [пглоread()](function.pg-lo-read.html)
    -   **пгlowrite()** [пглоwrite()](function.pg-lo-write.html)
    -   **пгloreadall()** [пглоreadall()](function.pg-lo-read-all.html)
    -   **пгloimport()** [пглоimport()](function.pg-lo-import.html)
    -   **пгloexport()** [пглоexport()](function.pg-lo-export.html)
    -   **пгsetclientencoding()** [пгsetclientencoding()](function.pg-set-client-encoding.html)
    -   **пгclientencoding()** -> [пгclientencoding()](function.pg-client-encoding.html)

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