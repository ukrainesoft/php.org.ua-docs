---
navigation:
  - mysqli.thread-id.md: '« mysqli::$threadід'
  - mysqli.use-result.md: 'mysqli::useresult »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::threadsafe'
---
# mysqli::threadsafe

# mysqlithreadsafe

(PHP 5, PHP 7, PHP 8)

mysqli::threadsafe -- mysqlithreadsafe — Показує, чи безпечна робота з процесами

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
