Форматує тимчасову мітку Unix

-   [« date\_timezone\_set](function.date-timezone-set.html)
    
-   [getdate »](function.getdate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции даты и времени](ref.datetime.html)
    
-   Форматує тимчасову мітку Unix
    

# date

(PHP 4, PHP 5, PHP 7, PHP 8)

date — Форматує тимчасову мітку Unix

### Опис

```methodsynopsis
date(string $format, ?int $timestamp = null): string
```

Повертає рядок, відформатований відповідно до зазначеного у параметрі `format` шаблон. Використовується позначка часу, задана параметром `timestamp` (мітка часу Unix), або поточний системний час, якщо параметр `timestamp` не заданий. Таким чином, параметр `timestamp` є необов'язковим і за умовчанням дорівнює значенню, що повертається функцією [time()](function.time.html)

Мітки часу Unix не обробляють часові пояси. Використовуйте клас [DateTimeImmutable](class.datetimeimmutable.html) та його метод форматування [DateTimeInterface::format()](datetime.format.html) для форматування інформації про дату/час з прив'язкою до часового поясу.

### Список параметрів

`format`

Прийнятий формат [DateTimeInterface::format()](datetime.format.html)

`timestamp`

Необов'язковий параметр `timestamp` являє собою мітку часу типу int, за умовчанням рівну поточному локальному часу, якщо `timestamp` не вказано або **`null`**. Іншими словами, значення за замовчуванням дорівнює результату функції [time()](function.time.html)

### Значення, що повертаються

Повертає відформатований рядок із датою. При передачі нечислового значення як параметр `timestamp` буде повернуто **`false`** та викликана помилка рівня **`E_WARNING`**

### Помилки

Кожен виклик до функцій дати/часу при неправильних налаштуваннях часового поясу згенерує помилку рівня **`E_WARNING`**, якщо часовий пояс неправильний. Дивіться також [date\_default\_timezone\_set()](function.date-default-timezone-set.html)

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `timestamp` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання функції **date()****

```php
<?php
// установка часового пояса по умолчанию.
date_default_timezone_set('UTC');


// выведет примерно следующее: Monday
echo date("l");

// выведет примерно следующее: Monday 8th of August 2005 03:12:46 PM
echo date('l jS \of F Y h:i:s A');

// выведет: July 1, 2000 is on a Saturday
echo "July 1, 2000 is on a " . date("l", mktime(0, 0, 0, 7, 1, 2000));

/* пример использования константы в качестве форматирующего параметра */
// выведет примерно следующее: Mon, 15 Aug 2005 15:12:46 UTC
echo date(DATE_RFC822);

// выведет примерно следующее: 2000-07-01T00:00:00+00:00
echo date(DATE_ATOM, mktime(0, 0, 0, 7, 1, 2000));
?>
```

Щоб заборонити розпізнавання символу як форматуючого, слід екранувати його за допомогою зворотного слішу. Якщо екранований символ також є послідовністю, що форматує, то слід екранувати його повторно.

**Приклад #2 Екранування символів у функції **date()****

```php
<?php
// выведет примерно следующее: Wednesday the 15th
echo date('l \t\h\e jS');
?>
```

Для виведення минулих та майбутніх дат зручно використовувати функції **date()** і [mktime()](function.mktime.html)

**Приклад #3 Приклад спільного використання функцій **date()** і [mktime()](function.mktime.html)**

```php
<?php
$tomorrow  = mktime(0, 0, 0, date("m")  , date("d")+1, date("Y"));
$lastmonth = mktime(0, 0, 0, date("m")-1, date("d"),   date("Y"));
$nextyear  = mktime(0, 0, 0, date("m"),   date("d"),   date("Y")+1);
?>
```

> **Зауваження**
> 
> Цей спосіб більш надійний, ніж просте віднімання та додавання секунд до мітки часу, оскільки дозволяє при необхідності гнучко здійснити перехід на літній/зимовий час.

Ще кілька прикладів використання функції **date()**. Важливо, що слід екранувати всі символи, які потрібно залишити без змін. Це справедливо і для тих символів, які в поточній версії PHP не розпізнаються як форматуючі, оскільки це може бути введено в наступних версіях. Для екранування керуючих послідовностей (наприклад, n) слід використовувати одинарні лапки.

**Приклад #4 Форматування з використанням **date()****

```php
<?php
// Предположим, что текущей датой является 10 марта 2001, 5:16:18 вечера,
// и мы находимся в часовом поясе Mountain Standard Time (MST)

$today = date("F j, Y, g:i a");                 // March 10, 2001, 5:16 pm
$today = date("m.d.y");                         // 03.10.01
$today = date("j, n, Y");                       // 10, 3, 2001
$today = date("Ymd");                           // 20010310
$today = date('h-i-s, j-m-y, it is w Day');     // 05-16-18, 10-03-01, 1631 1618 6 Satpm01
$today = date('\i\t \i\s \t\h\e jS \d\a\y.');   // it is the 10th day.
$today = date("D M j G:i:s T Y");               // Sat Mar 10 17:16:18 MST 2001
$today = date('H:m:s \m \i\s\ \m\o\n\t\h');     // 17:03:18 m is month
$today = date("H:i:s");                         // 17:16:18
$today = date("Y-m-d H:i:s");                   // 2001-03-10 17:16:18 (формат MySQL DATETIME)
?>
```

Для форматування дат іншими мовами замість функції **date()** можна використовувати метод [IntlDateFormatter::format()](intldateformatter.format.html)

### Примітки

> **Зауваження**
> 
> Для отримання мітки часу з строкового представлення дати можна скористатися функцією [strtotime()](function.strtotime.html). Крім того, деякі бази даних мають власні функції для перетворення внутрішнього подання дати на мітку часу (наприклад, функція MySQL [» UNIX\_TIMESTAMP](http://dev.mysql.com/doc/mysql/en/date-and-time-functions.html)

**Підказка**

Тимчасову позначку початку запиту можна отримати з поля [$\_SERVER\['REQUEST\_TIME'\]](reserved.variables.server.html)

### Дивіться також

-   [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.html) - Повертає новий об'єкт DateTimeImmutable
-   [DateTimeInterface::format()](datetime.format.html) - Повертає дату, відформатовану згідно з переданим форматом
-   [gmdate()](function.gmdate.html) - Форматує дату/час за Грінвічем
-   [idate()](function.idate.html) - Перетворює локальний час/дату на ціле число
-   [getdate()](function.getdate.html) - Повертає інформацію про дату/час
-   [getlastmod()](function.getlastmod.html) - Отримує час останньої модифікації сторінки
-   [mktime()](function.mktime.html) - Повертає позначку часу Unix для заданої дати
-   [IntlDateFormatter::format()](intldateformatter.format.html) - Форматує значення дати/часу у вигляді рядка
-   [time()](function.time.html) - Повертає поточну мітку системного часу Unix
-   [Предопределённые константы даты и времени](class.datetimeinterface.html#datetime.constants.types)