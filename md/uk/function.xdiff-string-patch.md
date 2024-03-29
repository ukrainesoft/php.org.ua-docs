---
navigation:
  - function.xdiff-string-patch-binary.md: « xdiff\_string\_patch\_binary
  - function.xdiff-string-rabdiff.md: xdiff\_string\_rabdiff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_patch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_patch

(PECL xdiff >= 0.2.0)

xdiff\_string\_patch — Застосувати звичайний патч до рядка

### Опис

```methodsynopsis
xdiff_string_patch(    string $str,    string $patch,    int $flags = ?,    string &$error = ?): string
```

Застосовує до рядка `str` звичайний патч `patch` та повертає результат . `patch` має бути звичайним патчем, створеним за допомогою функцій [xdiff\_file\_diff()](function.xdiff-file-diff.md) або [xdiff\_string\_diff()](function.xdiff-string-diff.md). Опціональний параметр `flags` задає режим операції. Усі відкинуті частини патчу будуть записані у змінну `error`

### Список параметрів

`str`

Оригінальний рядок.

`patch`

Стандартний патч. Повинен бути створений функціями [xdiff\_string\_diff()](function.xdiff-string-diff.md), или[xdiff\_file\_diff()](function.xdiff-file-diff.md)або за допомогою інструментів, що створюють сумісні патчі.

`flags`

`flags` може бути **`XDIFF_PATCH_NORMAL`** (режим за замовчуванням, нормальний патч) або **`XDIFF_PATCH_REVERSE`** (Реверсивний патч).

Починаючи з версії 1.5.0, можна використовувати бінарне АБО для додавання прапора. **`XDIFF_PATCH_IGNORESPACE`**

`error`

Якщо заданий, то цю змінну будуть записані всі відкинуті частини патча.

### Значення, що повертаються

Повертає рядок, або \*\*`false`\*\*в случае возникновения ошибке.

### Приклади

**Приклад #1 Приклад використання** xdiff\_string\_patch()\*\*\*\*

Наступний код застосовує патч до статті.

```php
<?php
$old_article = file_get_contents('./old_article.txt');
$diff = $_SERVER['patch']; /* Допустим кто-то отправил патч через html-форму */

$errors = '';

$new_article = xdiff_string_patch($old_article, $diff, XDIFF_PATCH_NORMAL, $errors);
if (is_string($new_article)) {
    echo "Новая статья:\n";
    echo $new_article;
}

if (strlen($errors)) {
    echo "Отклонены: \n";
    echo $errors;
}

?>
```

### Дивіться також

-   [xdiff\_string\_diff()](function.xdiff-string-diff.md) \- Створити звичайний патч для двох рядків
