---
navigation:
  - function.gmp-binomial.md: « gmp\_binomial
  - function.gmp-cmp.md: gmp\_cmp »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_clrbit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_clrbit

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_clrbit - Скидання біта

### Опис

```methodsynopsis
gmp_clrbit(GMP $num, int $index): void
```

Скидає (встановлює 0) біт на позиції `index`аргумента`num`. Індексація починається із 0.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md)

`index`

Індекс біта, що очищається. Індекс 0 вказує на молодший біт.

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_clrbit()\*\*\*\*

```php
<?php
    $a = gmp_init("0xff");
    gmp_clrbit($a, 0); // индексация с 0, младший значащий бит
    echo gmp_strval($a) . "\n";
    ?>
```

Результат виконання наведеного прикладу:

```
254
```

### Примітки

> **Зауваження** :
> 
> На відміну від більшості GMP функцій, **gmp\_clrbit()** має викликатися для вже існуючого об'єкта GMP (наприклад, створеного за допомогою [gmp\_init()](function.gmp-init.md)). Функція не створює їх автоматично.

### Дивіться також

-   [gmp\_setbit()](function.gmp-setbit.md) \- Встановлення біта
-   [gmp\_testbit()](function.gmp-testbit.md) \- Перевірка, чи встановлений біт в 1
