---
navigation:
  - function.fann-copy.html: « fanncopy
  - function.fann-create-shortcut-array.html: fanncreateshortcutarray »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncreatefromfile
---
# fanncreatefromfile

(PECL fann> = 1.0.0)

fanncreatefromfile — Створює нейронну мережу із зворотним розповсюдженням помилки з конфігураційного файлу

### Опис

```methodsynopsis
fann_create_from_file(string $configuration_file): resource
```

Створює нейронну мережу зі зворотним поширенням помилки з конфігураційного файлу, створеного раніше за допомогою [fannsave()](function.fann-save.md)

### Список параметрів

`configuration_file`

Конфігураційний файл.

### Значення, що повертаються

Повертає ресурс (resource) нейронної мережі у разі успішного виконання, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsave()](function.fann-save.md) - Зберігає всю мережу файл конфігурації
