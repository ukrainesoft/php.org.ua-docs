- [«Звернення до функцій через змінні](functions.variable-functions.md)
- [Анонімні функції»](functions.anonymous.md)

- [PHP Manual](index.md)
- [Функції](language.functions.md)
- Вбудовані функції

## Вбудовані функції

У самому PHP міститься досить велика кількість вбудованих функцій
та мовних конструкцій. Також є функції, які вимагають, щоб PHP
був зібраний з певними модулями, інакше будуть
генеруватися фатальні помилки, спричинені використанням невідомої
функції. Наприклад, для того, щоб використовувати [функції для роботи з зображеннями](ref.image.md), наприклад,
[imagecreatetruecolor()](function.imagecreatetruecolor.md), необхідно
зібрати PHP за допомогою GD. Або ж для того, щоб скористатися
функцією [mysqli_connect()](function.mysqli-connect.md), необхідна
підтримка модуля [MySQLi](book.mysqli.md). Тим не менш, є багато
вбудованих функцій, які завжди доступні: наприклад, [функції обробки рядків](ref.strings.md) та [функції для роботи з змінними](ref.var.md). Викликавши [phpinfo()](function.phpinfo.md)
або [get_loaded_extensions()](function.get-loaded-extensions.md),
можна дізнатися, підтримка яких модулів є у використовуваному PHP. Також
слід врахувати, що підтримка деяких додаткових модулів увімкнена
за замовчуванням, і що сама документація до PHP розбита за модулями.
Ознайомтеся з розділами [Конфігурація](configuration.md),
[Установка](install.md), а також з документацією безпосередньо до
додатковим модулям для отримання більш детальної інформації про те,
як настроїти PHP.

Більш детальну інформацію про те, як слід читати та інтерпретувати
прототипи функцій, ви можете знайти в розділі [Як читати визначення функції](about.prototypes.md). Дуже важливо розуміти, що повертає
функція, або як саме вона модифікує передані аргументи.
Наприклад, функція [str_replace()](function.str-replace.md) повертає
модифікований рядок, у той час як функція
[usort()](function.usort.md) працює з фактично переданою
змінної. Кожна сторінка документації також містить інформацію,
яка специфічна для цієї функції, наприклад, інформацію про
параметрах, що змінюються в поведінці, значеннях, що повертаються.
у разі як вдалого, так і невдалого виконання, доступності функції
у різних версіях. Знання та застосування цих (іноді навіть непомітних)
нюансів дуже важливо для написання коректного PHP-коду.

> **Примітка**: Якщо функцію передаються не ті аргументи, які вона
> очікує, наприклад, масив (array) замість рядка (string), що повертається
> значення функції не визначено. Швидше за все в цьому випадку буде
> повернено **`null`**, але це просто угода, на неї не можна
> покладатися. Починаючи з PHP 8.0.0, у цьому випадку має бути викинуто
> виняток [TypeError](class.typeerror.md).

> **Примітка**:
>
> Скалярні типи для вбудованих функцій за замовчуванням
> що допускають значення **`null`** у примусовому режимі. Починаючи з
> PHP 8.1.0, передача **`null`** у параметр вбудованої функції, який
> не оголошений як допускає значення **`null`**, не рекомендується і в
> примусовому режимі видається повідомлення про старіння, щоб
> відповідати поведінці функцій користувача, де скалярні типи
> повинні бути явно позначені як такі, що допускають значення **`null`**.
>
> Наприклад, функція [strlen()](function.strlen.md) очікує, що
> параметр `$string` буде рядком (string), що не допускає значення
> **`null`**. З історичних причин PHP дозволяє передавати
> **`null`** для цього параметра в примусовому режимі та параметр
> неявно наводиться до рядка (string), у результаті виходить
> значення ``````. У строгому режимі викидається виняток
> [TypeError](class.typeerror.md).
>
> ` <?phpvar_dump(strlen(null));// "Deprecated: Passing null to parameter #1 ($string) of type string is deprecated" починаючи с PHP 8.1.0// foobar", null));// "Deprecated: Passing null to parameter #2 ($needle) of type string is deprecated" починаючи з PHP 8.1.0// bool(true

### Дивіться також

- [function_exists()](function.function-exists.md)
- [довідник функцій](funcref.md)
- [get_extension_funcs()](function.get-extension-funcs.md)
- [dl()](function.dl.md)
