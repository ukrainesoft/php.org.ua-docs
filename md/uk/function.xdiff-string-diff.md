---
navigation:
  - function.xdiff-string-diff-binary.md: « xdiff\_string\_diff\_binary
  - function.xdiff-string-merge3.md: xdiff\_string\_merge3 »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_diff
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_diff

(PECL xdiff >= 0.2.0)

xdiff\_string\_diff — Створити звичайний патч для двох рядків

### Опис

```methodsynopsis
xdiff_string_diff(    string $old_data,    string $new_data,    int $context = 3,    bool $minimal = false): string
```

Створює патч для рядків `old_data`и`new_data`. Підсумковий патч людиночитаємо. Опціональний параметр `context` вказує, скільки рядків контексту має бути додано до патчу навколо кожної відмінності. Встановлення параметра `minimal`в значение\*\*`true`\*\*позволит получить максимально короткий патч (может занять много времени).

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

Повертає рядок з патчем, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**xdiff\_string\_diff()\*\*\*\*

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

> **Зауваження** :
> 
> Ця функція не призначена для роботи з бінарними даними. Для бінарного порівняння використовуйте [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md) і [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md)

### Дивіться також

-   [xdiff\_string\_patch()](function.xdiff-string-patch.md) \- Застосувати звичайний патч до рядка
