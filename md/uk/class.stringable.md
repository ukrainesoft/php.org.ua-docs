---
navigation:
  - weakmap.offsetunset.md: '« WeakMap::offsetUnset'
  - stringable.tostring.md: 'Stringable::\_\_toString »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Інтерфейс Stringable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Stringable

(PHP 8)

## Вступ

Інтерфейс **Stringable**обозначает класс, реализующий метод[\_\_toString()](language.oop5.magic.md#object.tostring). На відміну від більшості інтерфейсів, **Stringable** неявно присутній у будь-якому класі, в якому визначено магічний метод [\_\_toString()](language.oop5.magic.md#object.tostring)хоча він може і повинен бути оголошений явно.

Його основне значення – дозволити функціям виконувати перевірку типу на відповідність об'єднаним типам `string|Stringable`, щоб приймати або рядковий примітив, або об'єкт, який може бути перетворений на рядок.

## Огляд інтерфейсів

```classsynopsis

    
     interface Stringable {

    /* Методы */
    
   public __toString(): string

   }
```

## Приклади використання Stringable

**Приклад #1 Простий приклад використання Stringable**

```php
<?php
class IPv4Address implements Stringable {
    private string $oct1;
    private string $oct2;
    private string $oct3;
    private string $oct4;

    public function __construct(string $oct1, string $oct2, string $oct3, string $oct4) {
        $this->oct1 = $oct1;
        $this->oct2 = $oct2;
        $this->oct3 = $oct3;
        $this->oct4 = $oct4;
    }

    public function __toString(): string {
        return "$this->oct1.$this->oct2.$this->oct3.$this->oct4";
    }
}

function showStuff(string|Stringable $value) {
    // Здесь Stringable будет преобразован в строку путем вызова
    // __toString.
    print $value;
}

$ip = new IPv4Address('123', '234', '42', '9');

showStuff($ip);
?>
```

Висновок наведеного прикладу буде схожим на:

```
123.234.42.9
```

## Зміст

-   [Stringable::\_\_function toString() { \[native code\] }](stringable.tostring.md)— Отримує рядкову виставу об'єкта
