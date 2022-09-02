---
navigation:
  - function.timezone-version-get.md: « timezoneversionget
  - datetime.formats.time.md: Формати времени »
  - index.md: PHP Manual
  - book.datetime.md: Дата/время
title: Допустимі формати дати/часу
---
# Допустимі формати дати/часу

## Зміст

-   [Формати времени](datetime.formats.time.md)
-   [Формати дати](datetime.formats.date.md)
-   [Складові форматів](datetime.formats.compound.md)
-   [Відносні формати](datetime.formats.relative.md)

У цьому розділі описуються всі різні формати, які приймає парсер: [DateTimeImmutable](class.datetimeimmutable.md) [DateTime](class.datetime.md) [datecreateimmutable()](function.date-create-immutable.md) [datecreate()](function.date-create.md) [dateparse()](function.date-parse.md) і [strtotime()](function.strtotime.md). Формати згруповані за розділами. У більшості випадків формати з різних розділів, розділені пробілом, комою або точкою, можуть використовуватися в одному і тому ж рядку дати/часу. Для кожного з підтримуваних форматів наведено один або кілька прикладів та опис формату. Символи в одинарних лапках нечутливі до регістру (`'t'` еквівалентно як `t`, так і `T`), символи в подвійних лапках чутливі до регістру (`"T"` означає тільки `T`

Слід взяти до уваги загальне склепіння правил.

1.  Парсер допускає кожної одиниці виміру (рік, місяць, день, година, хвилина, секунда) повний діапазон значень. Для року це всього 4 цифри, для місяця – 0-12, дня – 0-31, для години – 0-24, а для хвилини – 0-59.
    
2.  Для секунд допускається значення 60, оскільки іноді рядки дати з цією секундою, що стрибає, дійсно з'являються. Але PHP реалізує час Unix, де "60" не є допустимим числом секунд і тому відбувається переповнення.
    
3.  Функція [strtotime()](function.strtotime.md) повертає **`false`**, якщо якесь число знаходиться поза діапазонами, а конструктор [DateTimeImmutable::construct()](datetimeimmutable.construct.md) викидає виняток.
    
4.  Якщо рядок містить дату, то всі елементи часу обнулюються до 0.
    
5.  Все менш значущі елементи часу скидаються до 0, якщо у цьому рядку є якась частина часу.
    
6.  Парсер не робить жодних перевірок, щоб зробити його швидше (і більш універсальним).
    
7.  Існує додаткова перевірка, якщо вказано недійсну дату:
    
    ```php
    <?php
    $res = date_parse("2015-09-31");
    var_dump($res["warnings"]);
    ?>
    ```
    
    Результат виконання цього прикладу:
    
    ```
    array(1) {
      [11] =>
      string(27) "The parsed date was invalid"
    }
    ```
    
8.  Крайні випадки вже можна обробити, для цього необхідно використати метод [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md), надаючи правильний формат.
    
    ```php
    <?php
    $res = DateTimeImmutable::createFromFormat("Y-m-d", "2015-09-34");
    var_dump($res);
    ```
    
    Результат виконання цього прикладу:
    
    ```
    class DateTime#1 (3) {
      public $date =>
      string(26) "2015-10-04 17:24:43.000000"
      public $timezone_type =>
      int(3)
      public $timezone =>
      string(13) "Europe/London"
    }
    ```
