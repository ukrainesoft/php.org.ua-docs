Обумовлені константи

-   [« Типы ресурсов](runkit7.resources.html)
    
-   [Функції runkit7 »](ref.runkit7.html)
    
-   [PHP Manual](index.html)
    
-   [runkit7](book.runkit7.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`RUNKIT7_IMPORT_FUNCTIONS`** (int)

[runkit7import()](function.runkit7-import.html) прапор, що вказує, що нормальні функції мають бути імпортовані із зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_METHODS`** (int)

[runkit7import()](function.runkit7-import.html) прапор, що вказує на те, що методи класу повинні бути імпортовані з зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_CONSTS`** (int)

[runkit7import()](function.runkit7-import.html) прапор, що вказує на те, що константи класу повинні бути імпортовані із зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_PROPS`** (int)

[runkit7import()](function.runkit7-import.html) прапор, що вказує на те, що стандартні властивості класу повинні бути імпортовані із зазначеного файлу.

**`RUNKIT7_IMPORT_CLASS_STATIC_PROPS`** (int)

[runkit7import()](function.runkit7-import.html) прапор, що вказує на те, що статичні властивості класу повинні бути імпортовані із зазначеного файлу. Доступно з Runkit 1.0.1.

**`RUNKIT7_IMPORT_CLASSES`** (int)

[runkit7import()](function.runkit7-import.html) прапор, що представляє побітове значення АБО константи **`RUNKIT7_IMPORT_CLASS_*`**

**`RUNKIT7_IMPORT_OVERRIDE`** (int)

[runkit7import()](function.runkit7-import.html) прапор, що вказує на те, що якщо якісь імпортовані функції, методи, константи або властивості вже існують, вони повинні бути замінені новими визначеннями. Якщо цей прапор не встановлений, будь-які імпортовані визначення, які вже існують, будуть відкинуті.

**`RUNKIT7_ACC_RETURN_REFERENCE`** (int)

Увімкніть цей прапор, щоб створювана або повторно оголошена функція або метод повертали посилання.

**`RUNKIT7_ACC_PUBLIC`** (int)

Прапор для [runkit7methodadd()](function.runkit7-method-add.html) і [runkit7methodredefine()](function.runkit7-method-redefine.html), щоб зробити метод публічним

**`RUNKIT7_ACC_PROTECTED`** (int)

Прапор для [runkit7methodadd()](function.runkit7-method-add.html) and [runkit7methodredefine()](function.runkit7-method-redefine.html), щоб зробити метод захищеним.

**`RUNKIT7_ACC_PRIVATE`** (int)

Прапор для [runkit7methodadd()](function.runkit7-method-add.html) and [runkit7methodredefine()](function.runkit7-method-redefine.html), щоб зробити метод приватним

**`RUNKIT7_ACC_STATIC`** (int)

Прапор для [runkit7methodadd()](function.runkit7-method-add.html) and [runkit7methodredefine()](function.runkit7-method-redefine.html)зробити метод статичним.

**`RUNKIT7_FEATURE_MANIPULATION`** (int)

дорівнює 1, якщо включена маніпуляція під час виконання і 0 в іншому випадку.

**`RUNKIT7_FEATURE_SUPERGLOBALS`** (int)

дорівнює 1, якщо користувацькі суперглобальні змінні включені і 0 в іншому випадку.

**`RUNKIT7_FEATURE_SANDBOX`** (int)

Завжди 0, неможливо продати функцію пісочниці в php 7.