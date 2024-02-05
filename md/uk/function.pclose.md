---
navigation:
  - function.pathinfo.md: « pathinfo
  - function.popen.md: popen »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: pclose
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pclose

(PHP 4, PHP 5, PHP 7, PHP 8)

pclose — Закриває файловий покажчик процесу

### Опис

```methodsynopsis
pclose(resource $handle): int
```

Закриває файловий покажчик на потік, відкритий за допомогою [popen()](function.popen.md)

### Список параметрів

`handle`

Файловий покажчик має бути чинним та повинен бути отриманий успішним викликом функції [popen()](function.popen.md)

### Значення, що повертаються

Повертає статус виходу процесу, що завершується. У разі виникнення помилки повертається `-1`

> **Зауваження** :
> 
> Якщо PHP зібрано з опцією --enable-sigchild, значення цієї функції, що повертається, не визначено.

### Приклади

**Пример #1 Пример использования**pclose()\*\*\*\*

```php
<?php
$handle = popen('/bin/ls', 'r');
pclose($handle);
?>
```

### Примітки

> **Зауваження** **Тільки для Unix:**
> 
> **pclose()** внутрішньо реалізована за допомогою системного виклику `waitpid(3)`. Для отримання реального коду виходу використовуйте натомість функцію [pcntl\_wexitstatus()](function.pcntl-wexitstatus.md)

### Дивіться також

-   [popen()](function.popen.md) \- Відкриває файловий покажчик процесу
