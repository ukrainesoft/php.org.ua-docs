Перетворення GMP числа в рядок

-   [« gmpsqrtrem](function.gmp-sqrtrem.html)
    
-   [gmpsub »](function.gmp-sub.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Перетворення GMP числа в рядок
    

# gmpstrval

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpstrval — Перетворення GMP числа на рядок

### Опис

```methodsynopsis
gmp_strval(GMP|int|string $num, int $base = 10): string
```

Перетворює GMP число в рядок у системі числення `base`. За замовчуванням числа перетворюються на десятирічну систему числення.

### Список параметрів

`num`

GMP число для конвертації.

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`base`

Система числення числа, що повертається. За замовчуванням - 10. Можливі значення: від 2 до 62 та від -2 до -36.

### Значення, що повертаються

Число у вигляді рядка (string).

### Приклади

**Приклад #1 Перетворення GMP числа в рядок**

```php
<?php
$a = gmp_init("0x41682179fbf5");
printf("Десятичное: %s, 36-ричное: %s", gmp_strval($a), gmp_strval($a,36));
?>
```