---
navigation:
  - gmp.constants.md: « Зумовлені константи
  - ref.gmp.md: GMP Функції »
  - index.md: PHP Manual
  - book.gmp.md: GMP
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Обчислення факторіалу за допомогою GMP**

```php
<?php
function fact($x)
{
    $return = 1;
    for ($i=2; $i <= $x; $i++) {
        $return = gmp_mul($return, $i);
    }
    return $return;
}

echo gmp_strval(fact(1000)) . "\n";
?>
```

Цей приклад досить швидко обчислить факторіал від 1000 (а це дуже багато).
