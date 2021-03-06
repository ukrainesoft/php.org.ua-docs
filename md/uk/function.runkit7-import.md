- [«runkit7_function_rename](function.runkit7-function-rename.md)
- [runkit7_method_add »](function.runkit7-method-add.md)

- [PHP Manual](index.md)
- [Функції runkit7](ref.runkit7.md)
- Обробляє функцію імпорту файлу PHP та визначення класів, при
необхідності перезаписуючи

# runkit7_import

(PECL runkit7 \>= Unknown)

runkit7_import — Обробляє функцію імпорту файлу PHP та визначення
класів, при необхідності перезаписуючи

**Увага**

Функціонал був *віддалений* у PECL runkit7 4.0.0.

### Опис

**runkit7_import**(string `$filename`, int `$flags` = ?): bool

Функція подібна до [include](function.include.md). Однак будь-який код,
що знаходиться поза межами функції або класу, просто ігнорується. Крім
того, в залежності від значення `flags`, будь-які функції чи класи,
які вже існують у поточному запущеному середовищі, можуть бути
автоматично перезаписані їх новими визначеннями.

### Список параметрів

`filename`
Ім'я файлу для імпорту визначень функцій та класів.

`flags`
Побітове АБО констант [`RUNKIT7_IMPORT_*`](runkit7.constants.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.
