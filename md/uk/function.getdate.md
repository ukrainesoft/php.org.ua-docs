- [« date](function.date.md)
- [gettimeofday »](function.gettimeofday.md)

- [PHP Manual](index.md)
- [Функції дати та часу](ref.datetime.md)
- Повертає інформацію про дату/час

# getdate

(PHP 4, PHP 5, PHP 7, PHP 8)

getdate — Повертає інформацію про дату/час

### Опис

**getdate**(?int `$timestamp` = **`null`**): array

Повертає асоціативний масив (array), що містить інформацію про дату,
представленою міткою часу `timestamp` або поточним системним
часом, якщо `timestamp` не був переданий або **`null`**.

### Список параметрів

`timestamp`
Необов'язковий параметр `timestamp` є міткою часу
типу int, за умовчанням рівну поточному локальному часу, якщо
`timestamp` не вказаний або **`null`**. Іншими словами, значення по
замовчування дорівнює результату функції [time()](function.time.md).

### Значення, що повертаються

Повертає асоціативний масив (array) з інформацією про параметр
`timestamp`, який містить такі елементи:

| Індекс Опис | Приклад значення                                                                                                                                                                                     |                                                                             |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| "seconds"   | Числове уявлення секунд                                                                                                                                                                              | від 0 до 59                                                                 |
| "minutes"   | Числове уявлення хвилин                                                                                                                                                                              | від 0 до 59                                                                 |
| "hours"     | Числове уявлення годинників                                                                                                                                                                          | від 0 до 23                                                                 |
| "mday"      | Порядковий номер дня місяця від 1 до 31                                                                                                                                                              |                                                                             |
| "wday"      | Порядковий номер дня тижня від 0 (неділя) до 6 (субота)                                                                                                                                              |                                                                             |
| mon'        | Порядковий номер місяця від 1 до 12                                                                                                                                                                  |                                                                             | | | |                                                                                                                                                                                                      
| "year"      | Номер року, 4 цифри Приклади: 1999, 2003                                                                                                                                                             |                                                                             |
| yday        | Порядковий номер дня року                                                                                                                                                                            | від 0 до 365                                                                | | | | |                                                                                                                                                                                                      
| "weekday"   | Повне найменування дня тижня від Sunday до Saturday                                                                                                                                                  |                                                                             |
| month'      | Повне найменування місяця, наприклад January або March                                                                                                                                               | від January до December                                                     |
| 0           | Кількість секунд, що пройшли з початку епохи Unix (The Unix Epoch), подібно до значення, що повертається функцією [time()](function.time.md) і використовуваною функцією [date()](function.date.md). | Залежить від платформи, в більшості випадків від -2147483648 до 2147483647. |

**Індекси асоціативного масиву, що повертається**

### Список змін

| Версія | Опис                                    |
| ------ | --------------------------------------- |
| 8.0.0  | timestamp тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання функції **getdate()****

` <?php$today = getdate();print_r($today);?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[seconds] => 40
[minutes] => 58
[hours] => 21
[mday] => 17
[wday] => 2
[mon] => 6
[year] => 2003
[yday] => 167
[weekday] => Tuesday
[month] => June
[0] => 1055901520
)

### Дивіться також

- [date()](function.date.md) - Форматує тимчасову мітку Unix
- [idate()](function.idate.md) - Перетворює локальний час/дату на
ціле число
- [localtime()](function.localtime.md) - Повертає локальний час
- [time()](function.time.md) - Повертає поточну мітку системного
часу Unix
- [setlocale()](function.setlocale.md) - Встановлює налаштування
локалі
