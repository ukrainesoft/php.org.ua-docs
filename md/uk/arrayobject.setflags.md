Встановлює прапори поведінки

-   [« ArrayObject::serialize](arrayobject.serialize.md)
    
-   [ArrayObject::setIteratorClass »](arrayobject.setiteratorclass.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayObject](class.arrayobject.md)
    
-   Встановлює прапори поведінки
    

# ArrayObject::setFlags

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ArrayObject::setFlags — Встановлює прапори поведінки

### Опис

```methodsynopsis
public ArrayObject::setFlags(int $flags): void
```

Встановлює прапори, які впливають на поведінку ArrayObject.

### Список параметрів

`flags`

Нова поведінка ArrayObject. Допускається або бітова маска, або названі константи. Використання іменованих констант рекомендується для забезпечення сумісності з майбутніми версіями.

Доступні прапори поведінки наведені нижче. Фактичні значення цих прапорів описані у розділі [Обумовлені константи](class.arrayobject.html#arrayobject.constants)

**Прапори поведінки ArrayObject**

| Значение | Константа                                                                                |
|----------|------------------------------------------------------------------------------------------|
|          | [ArrayObject::STDPROPLIST](class.arrayobject.html#arrayobject.constants.std-prop-list)   |
|          | [ArrayObject::ARRAYАСPROPS](class.arrayobject.html#arrayobject.constants.array-as-props) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::setFlags()****

```php
<?php
// Масив с доступными фруктами
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Попытка использовать ключ Масива как свойство
var_dump($fruitsArrayObject->lemons);
// Установка флага, позволяющего использовать ключи Масива как свойства ArrayObject
$fruitsArrayObject->setFlags(ArrayObject::ARRAY_AS_PROPS);
// Новая попытка
var_dump($fruitsArrayObject->lemons);
?>
```

Результат виконання цього прикладу:

```
NULL
int(1)
```