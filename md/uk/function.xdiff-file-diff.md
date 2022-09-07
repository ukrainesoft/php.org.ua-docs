---
navigation:
  - function.xdiff-file-diff-binary.md: xdifffilediffbinary
  - function.xdiff-file-merge3.md: xdifffilemerge3 »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdifffilediff
---
# xdifffilediff

(PECL xdiff >= 0.2.0)

xdifffilediff — Створити уніфікований патч із порівняння двох файлів

### Опис

```methodsynopsis
xdiff_file_diff(    string $old_file,    string $new_file,    string $dest,    int $context = 3,    bool $minimal = false): bool
```

Створює уніфікований патч, що містить відмінності двох файлів `old_file` і `new_file` та зберігає його у файл `dest`. Результат людиночитаний. Необов'язковий параметр `context` вказує, скільки рядків контексту має бути додано навколо кожного зміненого рядка. Завдання параметра `minimal` рівним **`true`** приведе до створення максимально короткого патчу, що може тривати багато часу.

### Список параметрів

`old_file`

Шлях до першого, "старого" файлу.

`new_file`

Шлях до другого, "нового" файлу.

`dest`

Шлях до файлу патчу.

`context`

Вказує, скільки рядків контексту необхідно включити до патчу.

`minimal`

Встановіть рівним \*\*`true`\*\*мінімізувати розмір патча. Може зайняти тривалий час.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **xdifffilediff()****

У наступному прикладі створюється уніфікований патч двох скриптів PHP з величиною контексту 2.

```php
<?php
$old_version = 'my_script.php';
$new_version = 'my_new_script.php';

xdiff_file_diff($old_version, $new_version, 'my_script.diff', 2);
?>
```

### Примітки

> **Зауваження**
> 
> З бінарними даними ця функція працює погано. Для бінарних патчів використовуйте [xdifffilebdiff()](function.xdiff-file-bdiff.md)[xdifffilerabdiff()](function.xdiff-file-rabdiff.md)

### Дивіться також

-   [xdifffilepatch()](function.xdiff-file-patch.md) - Застосування уніфікованого патчу до файлу
