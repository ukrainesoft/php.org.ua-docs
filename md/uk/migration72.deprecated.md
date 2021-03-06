- [« Зміни, що ламають зворотну сумісність](migration72.incompatible.md)
- [Інші зміни »](migration72.other-changes.md)

- [PHP Manual](index.md)
- [Міграція з PHP 7.1.x на PHP 7.2.x](migration72.md)
- Функціонал, оголошений застарілим у PHP 7.2.x

## Функціонал, оголошений застарілим у PHP 7.2.x

### Рядки без лапок

Рядки без лапок, які не є існуючими глобальними
константами, вважалися за рядки. Така поведінка раніше викликала помилку
рівня **`E_NOTICE`**, але тепер буде **`E_WARNING`**. У наступному
основної версії PHP замість помилки викидатиметься виняток
[Error](class.error.md).

`<?phpvar_dump(NONEXISTENT);/* Висновок:Warning:Use of undefined constant NONEXISTENT - assumed 'NONEXISTENT' (this will throw an Error in a          */ `

### [png2wbmp()](function.png2wbmp.md) та [jpeg2wbmp()](function.jpeg2wbmp.md)

Функції [png2wbmp()](function.png2wbmp.md) та
[jpeg2wbmp()](function.jpeg2wbmp.md) з модуля GD оголошені
застарілими та будуть видалені у наступній основній версії PHP.

### Варіант **`INTL_IDNA_VARIANT_2003`**

У модулі Intl оголошено застарілим варіант **`INTL_IDNA_VARIANT_2003`**,
який в даний час використовується за замовчуванням для функцій
[idn_to_ascii()](function.idn-to-ascii.md) та
[idn_to_utf8()](function.idn-to-utf8.md). У PHP 7.4 значення по
замовчуванням буде змінено на **`INTL_IDNA_VARIANT_UTS46`**, а в наступному
основної версії PHP константа **`INTL_IDNA_VARIANT_2003`** буде
повністю видалено.

### Функція [\_\_autoload()](function.autoload.md)

Функція [\_\_autoload()](function.autoload.md) була оголошена
застарілої, тому що вона поступається альтернативною функцією
[spl_autoload_register()](function.spl-autoload-register.md) (через
того, що не може мати чергу з функцій автозавантаження), і тому
що немає сумісності між цими двома стилями автозавантаження.

### Параметр `track_errors` та змінна `$php_errormsg`

Коли параметр `track_errors` включений в ini-налаштуваннях, змінна
`$php_errormsg` створюється в локальній області видимості, коли
відбувається не фатальна помилка. Враховуючи, що кращим способом
отримання такої інформації про помилку є використання функції
[error_get_last()](function.error-get-last.md), дана можливість
була оголошена застарілою.

### Функція [create_function()](function.create-function.md)

Враховуючи проблеми з безпекою цієї функції (через те, що вона
є обгорткою над [eval()](function.eval.md)), ця функція
оголошено застарілою. Переважною альтернативою є
використання [анонімних функцій](functions.anonymous.md).

### Параметр `mbstring.func_overload`

Враховуючи проблеми сумісності рядкових функцій, що використовуються в
оточеннях із включеним цим параметром, цей параметр оголошений
застарілим.

### Приведення типу `(unset)`

Приведення будь-якого виразу з використанням цього типу завжди наводить
до **`null`**, і тому цей надлишковий тип приведення оголошено
застарілим.

### [parse_str()](function.parse-str.md) без другого параметра

Без передачі другого параметра функції
[parse_str()](function.parse-str.md), параметри рядка запиту будуть
заповнювати поточну таблицю символів (будуть доступні як змінні в
локальної області видимості). Враховуючи наслідки безпеки
через це, використання [parse_str()](function.parse-str.md) без
другого параметра оголошено застарілим. Ця функція завжди повинна
використовуватися з двома аргументами, тому що в другому аргументі
зберігаються параметри рядка запиту як елементи масиву.

### Функція [gmp_random()](function.gmp-random.md)

Ця функція генерує випадкове число, засноване на діапазоні, який
обчислюється залежно від платформи розміру лімба (limb). Через
цього ця функція оголошена застарілою. Переважним способом
генерації випадкового числа через модуль GMP є використання
функцій [gmp_random_bits()](function.gmp-random-bits.md) та
[gmp_random_range()](function.gmp-random-range.md).

### Функція [each()](function.each.md)

Ця функція набагато повільніша за ітерацією, ніж використання звичайного
`foreach`, і створює проблеми з реалізацією для деяких змін
мови, тому ця функція оголошена застарілою.

### [assert()](function.assert.md) з рядковим аргументом

Використання [assert()](function.assert.md) з рядковим параметром
вимагало передачі рядка для виконання [eval()](function.eval.md).
Враховуючи можливість віддаленого виконання коду, використання
[assert()](function.assert.md) з рядковим аргументом тепер
оголошено застарілим на користь використання логічних виразів.

### Аргумент `$errcontext` в обробниках помилок

Аргумент $errcontext містить всі локальні змінні в місці, де
була відбулася помилка. Враховуючи рідкісне його використання та проблеми,
пов'язані з внутрішньою оптимізацією, цей параметр оголошено застарілим.
Натомість рекомендується використовувати відладчик для отримання
інформації про помилки.

### Функція [read_exif_data()](function.read-exif-data.md)

Псевдонім [read_exif_data()](function.read-exif-data.md) був оголошений
застарілим на користь функції
[exif_read_data()](function.exif-read-data.md).
