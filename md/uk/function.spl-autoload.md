---
navigation:
  - function.spl-autoload-unregister.md: « spl\_autoload\_unregister
  - function.spl-classes.md: spl\_classes »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: spl\_autoload
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# spl\_autoload

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

spl\_autoload — Реализация по умолчанию метода\_\_autoload()

### Опис

```methodsynopsis
spl_autoload(string $class, ?string $file_extensions = null): void
```

Ця функція являє собою базову реалізацію методу [\_\_autoload()](function.autoload.md)Если она не указана и[spl\_autoload\_register()](function.spl-autoload-register.md) викликається без будь-яких параметрів, то при кожному наступному виклику [\_\_autoload()](function.autoload.md) використовуватиметься саме ця функція.

### Список параметрів

`class`

Ім'я класу (і простору імен), яке потрібно завантажити.

`file_extensions`

За замовчуванням функція шукатиме файли з розширеннями .inc та .php. по всіх include-шляхах, де може розташовуватися клас, що шукається.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викликає виняток [LogicException](class.logicexception.md), якщо клас не знайдено та відсутні інші зареєстровані автозавантажувачі.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `file_extensions` тепер допускає значення null. |
