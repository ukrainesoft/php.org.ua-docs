Реалізація за умовчанням методу autoload()

-   [« spl\_autoload\_unregister](function.spl-autoload-unregister.html)
    
-   [spl\_classes »](function.spl-classes.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SPL](ref.spl.html)
    
-   Реалізація за умовчанням методу autoload()
    

# splautoload

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoload — Реалізація за замовчуванням методу autoload()

### Опис

```methodsynopsis
spl_autoload(string $class, ?string $file_extensions = null): void
```

Ця функція являє собою базову реалізацію методу [\_\_autoload()](function.autoload.html). Якщо вона не вказана та [spl\_autoload\_register()](function.spl-autoload-register.html) викликається без будь-яких параметрів, то при кожному наступному виклику [\_\_autoload()](function.autoload.html) використовуватиметься саме ця функція.

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

| Версия | Описание                                        |
|--------|-------------------------------------------------|
|        | `file_extensions` тепер допускає значення null. |