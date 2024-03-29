---
navigation:
  - function.mcrypt-generic-init.md: « mcrypt\_generic\_init
  - function.mcrypt-get-block-size.md: mcrypt\_get\_block\_size »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_generic
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_generic

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_generic — Функція шифрує дані

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_generic(resource $td, string $data): string
```

Ця функція шифрує дані. Дані будуть доповнені символами`\0`" для того, щоб їх розмір став кратним розміру блоку. Ця функція повертає зашифровані дані. Зверніть увагу, що довжина рядка, що повертається, може бути більше вихідної через доповнення.

Якщо ви хочете зберігати шифровані дані в базі даних, переконайтеся, що ви зберігаєте рядок повністю, як вона була повернута цією функцією, інакше ви потім не зможете її розшифрувати. Якщо ваш оригінальний рядок був 10 символів довжиною, а розмір блоку дорівнює 8 (використовуйте [mcrypt\_enc\_get\_block\_size()](function.mcrypt-enc-get-block-size.md) для визначення розміру блоку) то розмір стовпця бази даних повинен бути як мінімум 16 символів. Зверніть увагу, що рядок повертається [mdecrypt\_generic()](function.mdecrypt-generic.md) також буде розміром 16 символів. У такому разі просто використовуйте rtrim($str, "\\0") для видалення доданих символів.

Наприклад, якщо ви збережете дані в MySQL, пам'ятайте, що при вставці значень поля типу VARCHAR, у них автоматично відкидаються пробіли з кінця рядка. Якщо зашифровані дані закінчуються на пробіл (ASCII 32), вони будуть пошкоджені при такій вставці. Найкраще використовуйте для зберігання поля типу TINYBLOB/TINYTEX або більше.

### Список параметрів

`td`

Дескриптор шифрування.

Обробник шифрування завжди повинен ініціалізуватися за допомогою [mcrypt\_generic\_init()](function.mcrypt-generic-init.md) з ключем та ініціалізуючим вектором перед викликом функції. Як тільки шифрування завершено, необхідно звільнити буфери шифрування шляхом виклику функції [mcrypt\_generic\_deinit()](function.mcrypt-generic-deinit.md)Смотрите Приклад в описании функции[mcrypt\_module\_open()](function.mcrypt-module-open.md)

`data`

Дані для шифрування.

### Значення, що повертаються

Повертає зашифровані дані.

### Дивіться також

-   [mdecrypt\_generic()](function.mdecrypt-generic.md) \- Дешифрування даних
-   [mcrypt\_generic\_init()](function.mcrypt-generic-init.md) \- Функція ініціалізує всі буфери, необхідні для шифрування
-   [mcrypt\_generic\_deinit()](function.mcrypt-generic-deinit.md) \- Ця функція деініціалізує модуль шифрування
