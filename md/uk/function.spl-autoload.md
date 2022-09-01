---
navigation:
  - function.spl-autoload-unregister.html: « splautoloadunregister
  - function.spl-classes.html: splclasses »
  - index.html: PHP Manual
  - ref.spl.html: Функції SPL
title: splautoload
---
# splautoload

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoload — Реалізація за замовчуванням методу autoload()

### Опис

```methodsynopsis
spl_autoload(string $class, ?string $file_extensions = null): void
```

Ця функція являє собою базову реалізацію методу [autoload()](function.autoload.html). Якщо вона не вказана та [splautoloadregister()](function.spl-autoload-register.html) викликається без будь-яких параметрів, то при кожному наступному виклику [autoload()](function.autoload.html) використовуватиметься саме ця функція.

### Список параметрів

`class`

Ім'я класу (і простору імен), яке потрібно завантажити.

`file_extensions`

За замовчуванням функція шукатиме файли з розширеннями .inc та .php. по всіх include-шляхах, де може розташовуватися клас, що шукається.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викликає виняток [LogicException](class.logicexception.html), якщо клас не знайдено та відсутні інші зареєстровані автозавантажувачі.

### список змін

| Версия | Описание |
| --- | --- |
|  | `file_extensions` тепер допускає значення null. |
