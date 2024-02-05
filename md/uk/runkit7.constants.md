---
navigation:
  - runkit7.resources.md: « Типи ресурсів
  - ref.runkit7.md: Функції runkit7 »
  - index.md: PHP Manual
  - book.runkit7.md: runkit7
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`RUNKIT7_IMPORT_FUNCTIONS`**(int)

[runkit7\_import()](function.runkit7-import.md) прапор, що вказує, що нормальні функції мають бути імпортовані із зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_METHODS`**(int)

[runkit7\_import()](function.runkit7-import.md) прапор, що вказує на те, що методи класу повинні бути імпортовані із зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_CONSTS`**(int)

[runkit7\_import()](function.runkit7-import.md) прапор, що вказує на те, що константи класу повинні бути імпортовані із зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_PROPS`**(int)

[runkit7\_import()](function.runkit7-import.md) прапор, що вказує на те, що стандартні властивості класу повинні бути імпортовані із зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_STATIC_PROPS`**(int)

[runkit7\_import()](function.runkit7-import.md) прапор, що вказує на те, що статичні властивості класу повинні бути імпортовані із зазначеного файлу. Доступно з Runkit 1.0.1.

**`RUNKIT7_IMPORT_CLASSES`**(int)

[runkit7\_import()](function.runkit7-import.md) прапор, що представляє побітове значення АБО константи **`RUNKIT7_IMPORT_CLASS_*`**

**`RUNKIT7_IMPORT_OVERRIDE`**(int)

[runkit7\_import()](function.runkit7-import.md) прапор, що вказує на те, що якщо якісь імпортовані функції, методи, константи або властивості вже існують, вони повинні бути замінені новими визначеннями. Якщо цей прапор не встановлений, будь-які імпортовані визначення, які вже існують, будуть відкинуті.

**`RUNKIT7_ACC_RETURN_REFERENCE`**(int)

Увімкніть цей прапор, щоб створювана або повторно оголошена функція або метод повертали посилання.

**`RUNKIT7_ACC_PUBLIC`**(int)

Флаг для[runkit7\_method\_add()](function.runkit7-method-add.md) і [runkit7\_method\_redefine()](function.runkit7-method-redefine.md), щоб зробити метод публічним

**`RUNKIT7_ACC_PROTECTED`**(int)

Флаг для[runkit7\_method\_add()](function.runkit7-method-add.md)and[runkit7\_method\_redefine()](function.runkit7-method-redefine.md), щоб зробити метод захищеним.

**`RUNKIT7_ACC_PRIVATE`**(int)

Флаг для[runkit7\_method\_add()](function.runkit7-method-add.md)and[runkit7\_method\_redefine()](function.runkit7-method-redefine.md), щоб зробити метод приватним

**`RUNKIT7_ACC_STATIC`**(int)

Флаг для[runkit7\_method\_add()](function.runkit7-method-add.md)and[runkit7\_method\_redefine()](function.runkit7-method-redefine.md)зробити метод статичним.

**`RUNKIT7_FEATURE_MANIPULATION`**(int)

дорівнює 1, якщо включена маніпуляція під час виконання і 0 в іншому випадку.

**`RUNKIT7_FEATURE_SUPERGLOBALS`**(int)

дорівнює 1, якщо користувацькі суперглобальні змінні включені і 0 в іншому випадку.

**`RUNKIT7_FEATURE_SANDBOX`**(int)

Завжди 0, неможливо продати функцію пісочниці в php 7.
