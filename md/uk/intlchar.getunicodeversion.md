Отримати версію Unicode

-   [« IntlChar::getPropertyValueName](intlchar.getpropertyvaluename.md)
    
-   [IntlChar::hasBinaryProperty »](intlchar.hasbinaryproperty.md)
    
-   [PHP Manual](index.md)
    
-   [IntlChar](class.intlchar.md)
    
-   Отримати версію Unicode
    

# IntlChar::getUnicodeVersion

(PHP 7, PHP 8)

IntlChar::getUnicodeVersion — Отримати версію Unicode

### Опис

```methodsynopsis
public static IntlChar::getUnicodeVersion(): array
```

Отримує інформацію про версію Unicode.

Масив, що повертається, заповнюється інформацією про версію Unicode використовуваної ICU. Наприклад, Unicode версії 3.1.1 поверне масив зі значеннями `[3, 1, 1, 0]`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив, що містить інформацію про версію Unicode.

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::getUnicodeVersion());
?>
```

Результат виконання цього прикладу:

```
array(4) {
  [0]=>
  int(7)
  [1]=>
  int(0)
  [2]=>
  int(0)
  [3]=>
  int(0)
}
```

### Дивіться також

-   [IntlChar::charAge()](intlchar.charage.md) - Отримати "вік" символьного коду