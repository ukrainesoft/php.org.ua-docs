- [« Налаштування під час виконання](pthreads.configuration.md)
- [Threaded »](class.threaded.md)

- [PHP Manual](index.md)
- [pthreads](book.pthreads.md)
- Обумовлені константи

# Зумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути
доступні лише в тому випадку, якщо PHP був зібраний за допомогою цього
модуля або в тому випадку, якщо даний модуль був динамічно завантажений
під час виконання.

**`PTHREADS_INHERIT_ALL`** (int)
Налаштування за промовчанням для всіх потоків, вказує pthreads копіювати
все оточення під час створення нового потоку (клас Thread)

**`PTHREADS_INHERIT_NONE`** (int)
Нічого не успадковувати при старті нового потоку

**`PTHREADS_INHERIT_INI`** (int)
Наслідувати INI-налаштування при старті нового потоку

**`PTHREADS_INHERIT_CONSTANTS`** (int)
Наслідувати користувальницькі константи при старті нового потоку

**`PTHREADS_INHERIT_CLASSES`** (int)
Наслідувати користувальницькі класи при старті нового потоку

**`PTHREADS_INHERIT_FUNCTIONS`** (int)
Успадкувати функції користувача при старті нового потоку

**`PTHREADS_INHERIT_INCLUDES`** (int)
Наслідувати інформацію з підключених файлів при старті нового потоку

**`PTHREADS_INHERIT_COMMENTS`** (int)
Наслідувати всі коментарі при старті нового потоку

**`PTHREADS_ALLOW_HEADERS`** (int)
Дозволяти потокам надсилати заголовки (headers) у стандартний висновок
(зазвичай заборонено)
