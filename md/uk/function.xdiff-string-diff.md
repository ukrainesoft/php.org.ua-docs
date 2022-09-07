---
navigation:
  - function.xdiff-string-diff-binary.md: xdiffstringdiffbinary
  - function.xdiff-string-merge3.md: xdiffstringmerge3 »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiffstringdiff
---
# xdiffstringdiff

(PECL xdiff >= 0.2.0)

xdiffstringdiff — Створити звичайний патч для двох рядків

### Опис

```methodsynopsis
xdiff_string_diff(    string $old_data,    string $new_data,    int $context = 3,    bool $minimal = false): string
```

Створює патч для рядків `old_data` і `new_data`. Підсумковий патч людину читаємо. Опціональний параметр `context` вказує, скільки рядків контексту має бути додано до патчу навколо кожної відмінності. Встановлення параметра `minimal` на значення **`true`** дозволить отримати максимально короткий патч (може зайняти багато часу).

### Список параметрів

`old_data`

Перший рядок із даними. Це будуть "старі" дані.

`new_data`

Другий рядок із даними. Це будуть "нові" дані.

`context`

Кількість рядків контексту навколо кожної зміни.

`minimal`

Якщо **`true`**, то буде створено максимально короткий патч (може зайняти багато часу).

### Значення, що повертаються

Повертає рядок з патчем, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **xdiffstringdiff()****

Наступний код виведе різницю двох статей.

```php
<?php
$old_article = file_get_contents('./old_article.txt');
$new_article = $_REQUEST['article']; /* Допустим кто-то отправил новую статью через html-форму */

$diff = xdiff_string_diff($old_article, $new_article, 1);
if (is_string($diff)) {
    echo "Различия в двух статьях:\n";
    echo $diff;
}

?>
```

### Примітки

> **Зауваження**
> 
> Ця функція не призначена для роботи з бінарними даними. Для бінарного порівняння використовуйте [xdiffstringbdiff()](function.xdiff-string-bdiff.md) і [xdiffstringrabdiff()](function.xdiff-string-rabdiff.md)

### Дивіться також

-   [xdiffstringpatch()](function.xdiff-string-patch.md) - Застосувати звичайний патч до рядка
