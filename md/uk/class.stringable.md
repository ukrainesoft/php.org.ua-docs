Інтерфейс Stringable

-   [« WeakMap::offsetUnset](weakmap.offsetunset.md)
    
-   [Stringable::toString »](stringable.tostring.md)
    
-   [PHP Manual](index.md)
    
-   [Вбудовані інтерфейси та класи](reserved.interfaces.md)
    
-   Інтерфейс Stringable
    

# Інтерфейс Stringable

(PHP 8)

## Вступ

Інтерфейс **Stringable** позначає клас, що реалізує метод [toString()](language.oop5.magic.html#object.tostring). На відміну від більшості інтерфейсів, **Stringable** неявно присутній у будь-якому класі, в якому визначено магічний метод [toString()](language.oop5.magic.html#object.tostring)хоча він може і повинен бути оголошений явно.

Його основне значення - дозволити функціям виконувати перевірку типу на відповідність типу union `string|Stringable`, щоб приймати або рядковий примітив, або об'єкт, який може бути перетворений на рядок.

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
class IPv4Address implements Stringable {
    private string $oct1;
    private string $oct2;
    private string $oct3;
    private string $oct4;

    public function __construct(string $oct1, string $oct2, string $oct3, string $oct4) {
        $this->oct1 = $oct1;
        $this->oct2 = $oct2;
        $this->oct3 = $oct3;
        $this->oct4 = $oct4;
    }

    public function __toString(): string {
        return "$this->oct1.$this->oct2.$this->oct3.$this->oct4";
    }
}

function showStuff(string|Stringable $value) {
    // Здесь Stringable будет преобразован в строку путем вызова
    // __toString.
    print $value;
}

$ip = new IPv4Address('123', '234', '42', '9');

showStuff($ip);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
123.234.42.9
```

## Зміст

-   [Stringable::toString](stringable.tostring.md) — Отримує рядкову виставу об'єкта