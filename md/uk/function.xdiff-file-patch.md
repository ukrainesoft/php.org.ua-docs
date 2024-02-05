---
navigation:
  - function.xdiff-file-patch-binary.md: « xdiff\_file\_patch\_binary
  - function.xdiff-file-rabdiff.md: xdiff\_file\_rabdiff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_file\_patch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_file\_patch

(PECL xdiff >= 0.2.0)

xdiff\_file\_patch — Використання уніфікованого патча до файлу

### Опис

```methodsynopsis
xdiff_file_patch(    string $file,    string $patch,    string $dest,    int $flags = DIFF_PATCH_NORMAL): mixed
```

Застосовує до файлу `file`патча`patch`и сохраняет результат в файл`patch` має бути уніфікованим патчем, створеним функціями [xdiff\_file\_diff()](function.xdiff-file-diff.md) [xdiff\_string\_diff()](function.xdiff-string-diff.md). Необов'язковий параметр `flags` задає режим операції.

### Список параметрів

`file`

Оригінальний файл.

`patch`

Уніфікований патч. Його можна створити функціями [xdiff\_string\_diff()](function.xdiff-string-diff.md) і [xdiff\_file\_diff()](function.xdiff-file-diff.md)або іншими сумісними інструментами.

`dest`

Шлях до результуючого файлу.

`flags`

Може бути **`XDIFF_PATCH_NORMAL`**(режим по умолчанию, нормальное создание патча) или\*\*`XDIFF_PATCH_REVERSE`\*\*(откат патча).

Починаючи з версії 1.5.0, ви можете використовувати побітове АБО для підключення прапора **`XDIFF_PATCH_IGNORESPACE`**

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо створення патчу пройшло успішно, рядок з відхиленими даними, якщо ні, і **`false`** у разі внутрішньої помилки.

### Приклади

**Приклад #1 Приклад використання** xdiff\_file\_patch()\*\*\*\*

Наступний код використовує уніфікований патч до файлу.

```php
<?php
$old_version = 'my_script-1.0.php';
$patch = 'my_script.patch';

$errors = xdiff_file_patch($old_version, $patch, 'my_script-1.1.php');
if (is_string($errors)) {
   echo "Отклонены:\n";
   echo $errors;
}

?>
```

**Приклад #2 Patch reversing example**

Наступний код застосовує відкат патча до файлу.

```php
<?php
$new_version = 'my_script-1.1.php';
$patch = 'my_script.patch';

$errors = xdiff_file_patch($new_version, $patch, 'my_script-1.0.php', XDIFF_PATCH_REVERSE);
if (is_string($errors)) {
   echo "Отклонены:\n";
   echo $errors;
}

?>
```

### Дивіться також

-   [xdiff\_file\_diff()](function.xdiff-file-diff.md) \- Створити уніфікований патч із порівняння двох файлів
