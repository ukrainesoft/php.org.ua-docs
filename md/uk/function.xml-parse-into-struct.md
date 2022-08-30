Розбір XML-даних та приміщення в масив

-   [« xmlgeterrorcode](function.xml-get-error-code.html)
    
-   [xmlparse »](function.xml-parse.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Розбір XML-даних та приміщення в масив
    

# xmlparseintostruct

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlparseintostruct - Розбір XML-даних та приміщення в масив

### Опис

```methodsynopsis
xml_parse_into_struct(    XMLParser $parser,    string $data,    array &$values,    array &$index = null): int
```

Ця функція розбирає XML-рядок і поміщає дані у 2 масиви. Масив `index` містить покажчики на розміщення значень у масиві `values`. Аргументи, що задають масиви, повинні передаватися на функцію за посиланням.

### Список параметрів

`parser`

Посилання на використовуваний XML-аналізатор.

`data`

Рядок XML-даних.

`values`

Масив значень XML даних.

`index`

Масив покажчиків на відповідні значення масиві $values.

### Значення, що повертаються

**xmlparseintostruct()** повертає 0 при невдалому розборі рядка та 1 при успішному. Це не те саме, що **`false`** і **`true`**, будьте обережні з такими операторами, як ===.

### список змін

| Версия | Описание                                                                                                    |
|--------|-------------------------------------------------------------------------------------------------------------|
|        | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікували ресурс (resource). |

### Приклади

Нижче наведено приклад, що демонструє внутрішній пристрій масивів, що генеруються функцією. XML-рядок містить простий тег `note` вкладений у тег `para`. Програма у прикладі розбирає цей рядок і виводить створені масиви:

**Приклад #1 Приклад використання **xmlparseintostruct()****

```php
<?php
$simple = "<para><note>простое примечание</note></para>";
$p = xml_parser_create();
xml_parse_into_struct($p, $simple, $vals, $index);
xml_parser_free($p);
echo "Массив index\n";
print_r($index);
echo "\nМассив vals\n";
print_r($vals);
?>
```

Після обробки програма виведе наступне:

```
Index array
Array
(
    [PARA] => Array
        (
            [0] => 0
            [1] => 2
        )

    [NOTE] => Array
        (
            [0] => 1
        )

)

Массив Vals
Array
(
    [0] => Array
        (
            [tag] => PARA
            [type] => open
            [level] => 1
        )

    [1] => Array
        (
            [tag] => NOTE
            [type] => complete
            [level] => 2
            [value] => простое примечание
        )

    [2] => Array
        (
            [tag] => PARA
            [type] => close
            [level] => 1
        )

)
```

Розбір, що управляється подіями (заснований на бібліотеці expat) може дати важкооброблюваний результат у разі, якщо розбирається складовий XML-документ. Ця функція не створює DOM-об'єктів, але масиви, що нею створюються, можна перетворити на деревоподібну структуру згодом. Таким чином, можна досить просто створювати об'єкти, що представляють вміст XML-файлу. Припустимо, що наступний XML файл представляє невелику базу даних з інформацією про амінокислоти:

**Приклад #2 moldb.xml – невелика база даних з інформацією про молекули**

Alanine ala `A` hydrophobic Lysine lys `K` charged

Код, який розбирає документ і створює відповідні об'єкти:

**Приклад #3 parsemoldb.php - розбирає moldb.xml і поміщає дані масив молекул**

```php
<?php

class AminoAcid {
    var $name;   // название аминокислоты
    var $symbol; // трёхбуквенное обозначение
    var $code;   // однобуквенный код
    var $type;   // гидрофобная, заряженная, нейтральная

    function __construct ($aa)
    {
        foreach ($aa as $k=>$v)
            $this->$k = $aa[$k];
    }
}

function readDatabase($filename)
{
    // чтение XML-базы данных аминокислот
    $data = file_get_contents($filename);
    $parser = xml_parser_create();
    xml_parser_set_option($parser, XML_OPTION_CASE_FOLDING, 0);
    xml_parser_set_option($parser, XML_OPTION_SKIP_WHITE, 1);
    xml_parse_into_struct($parser, $data, $values, $tags);
    xml_parser_free($parser);

    // проход через структуры
    foreach ($tags as $key=>$val) {
        if ($key == "molecule") {
            $molranges = $val;
            // каждая смежная пара значений массивов является верхней и
            // нижней границей определения молекулы
            for ($i=0; $i < count($molranges); $i+=2) {
                $offset = $molranges[$i] + 1;
                $len = $molranges[$i + 1] - $offset;
                $tdb[] = parseMol(array_slice($values, $offset, $len));
            }
        } else {
            continue;
        }
    }
    return $tdb;
}

function parseMol($mvalues)
{
    for ($i=0; $i < count($mvalues); $i++) {
        $mol[$mvalues[$i]["tag"]] = $mvalues[$i]["value"];
    }
    return new AminoAcid($mol);
}

$db = readDatabase("moldb.xml");
echo "** База данных аминокислот:\n";
print_r($db);

?>
```

Після виконання parsemoldb.php змінна $db містить масив об'єктів **AminoAcid**, А висновок відповідно наступний:

```
** База данных аминокислот:
Array
(
    [0] => aminoacid Object
        (
            [name] => Alanine
            [symbol] => ala
            [code] => A
            [type] => hydrophobic
        )

    [1] => aminoacid Object
        (
            [name] => Lysine
            [symbol] => lys
            [code] => K
            [type] => charged
        )

)
```