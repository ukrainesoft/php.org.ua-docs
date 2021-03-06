- [«Mhash](book.mhash.md)
- [Встановлення та налаштування »](mhash.setup.md)

- [PHP Manual](index.md)
- [Mhash](book.mhash.md)
-   Вступ

# Вступ

Ці функції призначені для роботи з
[»mhash](http://mhash.sourceforge.net/). Mhash може використовуватися для
підрахунку контрольних сум, хеш-сум, кодів ідентифікації повідомлень тощо
далі.

Це інтерфейс для бібліотеки mhash. Mhash підтримує велике
кількість алгоритмів шифрування, таких як MD5, SHA1, GOST та багатьох
інших. Для повного списку підтримуваних алгоритмів шифрування
Перейдіть до сторінки з [константами](mhash.constants.md). Для
отримання доступу до певного алгоритму з PHP потрібно використовувати
**`MHASH_hashname`**. Наприклад, щоб отримати доступ до TIGER необхідно
використовувати константу **`MHASH_TIGER`**.

> **Примітка**:
>
> Даний модуль застарів, використовуйте як заміну
> [Hash](book.hash.md).

> **Примітка**:
>
> Починаючи з PHP 7.0.0, модуль Mhash повністю інтегрований у модуль
> [Hash](book.hash.md). Таким чином, тепер не можна визначити
> доступність підтримки Mhash за допомогою функції
> [extension_loaded()](function.extension-loaded.md); замість неї
> використовуйте [function_exists()](function.function-exists.md). Крім
> того, Mhash більше не буде виводитися за допомогою
> [get_loaded_extensions()](function.get-loaded-extensions.md) та
> подібні функції.
