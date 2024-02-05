---
navigation:
  - function.wddx-serialize-value.md: « wddx\_serialize\_value
  - book.xmldiff.md: XMLDiff »
  - index.md: PHP Manual
  - ref.wddx.md: Функції WDDX
title: wddx\_serialize\_vars
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wddx\_serialize\_vars

(PHP 4, PHP 5, PHP 7)

wddx\_serialize\_vars — Серіалізація змінних у пакет WDDX

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_serialize_vars(mixed $var_name, mixed ...$var_names): string
```

Створює пакет WDDX із структурою, що містить серіалізоване уявлення переданих змінних.

### Список параметрів

Функція приймає змінну кількість параметрів.

`var_name`

Може бути або рядком, що означає змінну, або масивом, що містить рядки з назвами змінних або інший масив і т.д.

`var_names`

### Значення, що повертаються

Повертає пакет WDDX або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**wddx\_serialize\_vars()\*\*\*\*

```php
<?php
$a = 1;
$b = 5.5;
$c = array("blue", "orange", "violet");
$d = "colors";

$clvars = array("c", "d");
echo wddx_serialize_vars("a", "b", $clvars);
?>
```

Результат виконання наведеного прикладу:

```
<wddxPacket version='1.0'><header/><data><struct><var name='a'><number>1</number></var>
<var name='b'><number>5.5</number></var><var name='c'><array length='3'>
<string>blue</string><string>orange</string><string>violet</string></array></var>
<var name='d'><string>colors</string></var></struct></data></wddxPacket>
```
