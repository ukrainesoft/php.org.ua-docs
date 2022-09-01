---
navigation:
  - luasandbox.getpeakmemoryusage.md: '« LuaSandbox::getPeakMemoryUsage'
  - luasandbox.getversioninfo.md: 'LuaSandbox::getVersionInfo »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::getProfilerFunctionReport'
---
# LuaSandbox::getProfilerFunctionReport

(PECL luasandbox >= 1.1.0)

LuaSandbox::getProfilerFunctionReport — Отримує дані профілювача

### Опис

```methodsynopsis
public LuaSandbox::getProfilerFunctionReport(int $units = LuaSandbox::SECONDS): array
```

Для екземпляра профілювання, раніше запущеного за допомогою [LuaSandbox::enableProfiler()](luasandbox.enableprofiler.md), отримайте звіт про вартість кожної функції.

Місячність unit, використовувана для вартості, визначається за $units parameter:

**`LuaSandbox::SAMPLES`**

Вимірювання кількості зразків.

**`LuaSandbox::SECONDS`**

Вимірювання процесорного часу за секунди.

**`LuaSandbox::PERCENT`**

Вимірювання відсотка процесорного часу.

### Список параметрів

`units`

Константа одиниці виміру.

### Значення, що повертаються

Повертає вимірювання профілювача, відсортовані в порядку зменшення, як асоціативний масив (array). Ключі - це імена функцій Lua (з вихідним файлом і рядком, визначеними в кутових дужках), значення - це вимірювання як ціле число (int) або число плаваючою комою (float).

> **Зауваження**
> 
> У Windows функція завжди повертає порожній масив. В операційних системах, які не підтримують **`CLOCK_THREAD_CPUTIME_ID`**, таких як FreeBSD та Mac OS X, функція буде повідомляти фактичний минулий час, а не час процесора.

### Приклади

**Приклад #1 Профіль коду Lua**

```php
<?php

// создание нового LuaSandbox
$sandbox = new LuaSandbox();

// начало профилирования
$sandbox->enableProfiler( 0.01 );

// ... Выполнение какого-то кода Lua ...

// получение данных профилирования
$data = $sandbox->getProfilerFunctionReport();

?>
```
