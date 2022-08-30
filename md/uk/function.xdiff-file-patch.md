Застосування уніфікованого патчу до файлу

-   [xdifffilepatchbinary](function.xdiff-file-patch-binary.html)
    
-   [xdifffilerabdiff »](function.xdiff-file-rabdiff.html)
    
-   [PHP Manual](index.md)
    
-   [Функції xdiff](ref.xdiff.md)
    
-   Застосування уніфікованого патчу до файлу
    

# xdifffilepatch

(PECL xdiff >= 0.2.0)

xdifffilepatch — Використання уніфікованого патча до файлу

### Опис

```methodsynopsis
xdiff_file_patch(    string $file,    string $patch,    string $dest,    int $flags = DIFF_PATCH_NORMAL): mixed
```

Застосовує до файлу `file` патча `patch` та зберігає результат у файл . `patch` має бути уніфікованим патчем, створеним функціями [xdifffilediff()](function.xdiff-file-diff.html)[xdiffstringdiff()](function.xdiff-string-diff.html). Необов'язковий параметр `flags` задає режим операції.

### Список параметрів

`file`

Оригінальний файл.

`patch`

Уніфікований патч. Його можна створити функціями [xdiffstringdiff()](function.xdiff-string-diff.html) і [xdifffilediff()](function.xdiff-file-diff.html)або іншими сумісними інструментами.

`dest`

Шлях до результуючого файлу.

`flags`

Може бути **`XDIFF_PATCH_NORMAL`** (режим за умовчанням, нормальне створення патчу) або **`XDIFF_PATCH_REVERSE`** (Відкат патчу).

Починаючи з версії 1.5.0, ви можете використовувати побітове АБО для підключення прапора **`XDIFF_PATCH_IGNORESPACE`**

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо створення патчу пройшло успішно, рядок з відхиленими даними, якщо ні, і **`false`** у разі внутрішньої помилки.

### Приклади

**Приклад #1 Приклад використання **xdifffilepatch()****

Наступний код використовує уніфікований патч до файлу.

```php
<?php
$old_version = 'my_script-1.0.php';
$patch = 'my_script.patch';

$errors = xdiff_file_patch($old_version, $patch, 'my_script-1.1.php');
if (is_string($errors)) {
   echo "Отклонены:\n";
   echo $errors;
}

?>
```

**Приклад #2 Patch reversing example**

Наступний код застосовує відкат патча до файлу.

```php
<?php
$new_version = 'my_script-1.1.php';
$patch = 'my_script.patch';

$errors = xdiff_file_patch($new_version, $patch, 'my_script-1.0.php', XDIFF_PATCH_REVERSE);
if (is_string($errors)) {
   echo "Отклонены:\n";
   echo $errors;
}

?>
```

### Дивіться також

-   [xdifffilediff()](function.xdiff-file-diff.html) - Створити уніфікований патч із порівняння двох файлів