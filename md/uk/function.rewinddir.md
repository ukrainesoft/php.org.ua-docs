---
navigation:
  - function.readdir.md: « readdir
  - function.scandir.md: scandir »
  - index.md: PHP Manual
  - ref.dir.md: Функції для роботи з каталогами
title: rewinddir
---
# rewinddir

(PHP 4, PHP 5, PHP 7, PHP 8)

rewinddir — Скинути дескриптор каталогу

### Опис

```methodsynopsis
rewinddir(?resource $dir_handle = null): void
```

Скидає поток каталогу, переданий у параметрі `dir_handle` таким чином, щоб той вказував на початок каталогу.

### Список параметрів

`dir_handle`

Ресурс (resource) дескриптора каталогу, який раніше був відкритий за допомогою функції [opendir()](function.opendir.md). Якщо дескриптор каталогу не вказано, мається на увазі останній дескриптор, який було відкрито за допомогою [opendir()](function.opendir.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dir_handle` тепер допускає значення null. |
