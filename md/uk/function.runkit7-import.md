---
navigation:
  - function.runkit7-function-rename.html: « runkit7functionrename
  - function.runkit7-method-add.html: runkit7methodadd »
  - index.html: PHP Manual
  - ref.runkit7.html: Функції runkit7
title: runkit7import
---
# runkit7import

(PECL runkit7> = Unknown)

runkit7import — Обробляє функцію імпорту файлу PHP та визначення класів, за потреби перезаписуючи

**Увага**

Функціонал був *віддалений* у PECL runkit7 4.0.0.

### Опис

```methodsynopsis
runkit7_import(string $filename, int $flags = ?): bool
```

Функція подібна [include](function.include.md). Однак будь-який код, який знаходиться за межами функції або класу, просто ігнорується. Крім того, залежно від значення `flags`, будь-які функції або класи, які вже існують у поточному запущеному середовищі, можуть бути автоматично перезаписані їх новими визначеннями.

### Список параметрів

`filename`

Ім'я файлу для імпорту визначень функцій та класів.

`flags`

Побітове АБО констант [`RUNKIT7_IMPORT_*`](runkit7.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
