---
navigation:
  - function.fann-copy.md: « fann\_copy
  - function.fann-create-shortcut-array.md: fann\_create\_shortcut\_array »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_create\_from\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_create\_from\_file

(PECL fann >= 1.0.0)

fann\_create\_from\_file — Створює нейронну мережу із зворотним розповсюдженням помилки з конфігураційного файлу

### Опис

```methodsynopsis
fann_create_from_file(string $configuration_file): resource
```

Створює нейронну мережу зі зворотним поширенням помилки з конфігураційного файлу, створеного раніше за допомогою [fann\_save()](function.fann-save.md)

### Список параметрів

`configuration_file`

Конфігураційний файл.

### Значення, що повертаються

Повертає ресурс (resource) нейронної мережі у разі успішного виконання, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_save()](function.fann-save.md) \- Зберігає всю мережу файл конфігурації
