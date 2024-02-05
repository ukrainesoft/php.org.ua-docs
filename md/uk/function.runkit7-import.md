---
navigation:
  - function.runkit7-function-rename.md: « runkit7\_function\_rename
  - function.runkit7-method-add.md: runkit7\_method\_add »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_import
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_import

(PECL runkit7 >= Unknown)

runkit7\_import — Обробляє функцію імпорту файлу PHP та визначення класів, за потреби перезаписуючи

**Увага**

Функціонал був *віддалений*в PECL runkit7 4.0.0.

### Опис

```methodsynopsis
runkit7_import(string $filename, int $flags = ?): bool
```

Функция подобна[include](function.include.md). Однак будь-який код, який знаходиться за межами функції або класу, просто ігнорується. Крім того, залежно від значення `flags`, будь-які функції або класи, які вже існують у поточному запущеному середовищі, можуть бути автоматично перезаписані їх новими визначеннями.

### Список параметрів

`filename`

Ім'я файлу для імпорту визначень функцій та класів.

`flags`

Побітове АБО констант [`RUNKIT7_IMPORT_*`](runkit7.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
