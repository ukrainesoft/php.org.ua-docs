---
navigation:
  - mysqli.thread-id.md: '« mysqli::$thread\_id'
  - mysqli.use-result.md: 'mysqli::use\_result »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::thread\_safe'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::thread\_safe

# mysqli\_thread\_safe

(PHP 5, PHP 7, PHP 8)

mysqli::thread\_safe -- mysqli\_thread\_safe — Показує, чи безпечна робота з процесами

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::thread_safe(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_thread_safe(): bool
```

Показує, що клієнтська бібліотека скомпільована як потокобезпечна чи ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо клієнтська бібліотека потокобезпечна, інакше **`false`**
