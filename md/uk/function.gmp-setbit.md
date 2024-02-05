---
navigation:
  - function.gmp-scan1.md: « gmp\_scan1
  - function.gmp-sign.md: gmp\_sign »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_setbit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_setbit

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_setbit - Встановлення біта

### Опис

```methodsynopsis
gmp_setbit(GMP $num, int $index, bool $value = true): void
```

Встановлює 1 біт з індексом `index`в числе`num`

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md)

`index`

Індекс встановлюваного біта. Індекс 0 вказує на молодший біт.

`value`

True для установки біта (установки в 1/включено); false для його очищення (установки 0/вимкнено).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_setbit()**\- 0 индекс**

```php
<?php
$a = gmp_init("2"); //
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 0); // 0b10 now becomes 0b11
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

Результат виконання наведеного прикладу:

```
2 -> 0b10
3 -> 0b11
```

**Пример #2 Пример использования**gmp\_setbit()**\- 1 индекс**

```php
<?php
$a = gmp_init("0xfd");
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 1); // index starts at 0
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

Результат виконання наведеного прикладу:

```
253 -> 0b11111101
255 -> 0b11111111
```

**Пример #3 Пример использования**gmp\_setbit()**очистка бита**

```php
<?php
$a = gmp_init("0xff");
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 0, false); // clear bit at index 0
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

Результат виконання наведеного прикладу:

```
255 -> 0b11111111
254 -> 0b11111110
```

### Примітки

> **Зауваження** :
> 
> На відміну від більшості GMP функцій, **gmp\_setbit()** має викликатися для вже існуючого об'єкта GMP (наприклад, створеного функцією [gmp\_init()](function.gmp-init.md)). Число не створюватиметься автоматично.

### Дивіться також

-   [gmp\_clrbit()](function.gmp-clrbit.md) \- Скидання біта
-   [gmp\_testbit()](function.gmp-testbit.md) \- Перевірка, чи встановлений біт в 1
