- [« tidy::getRelease](tidy.getrelease.md)
- [tidy::head »](tidy.head.md)

- [PHP Manual](index.md)
- [Tidy](class.tidy.md)
- набуває статусу зазначеного документа

# tidy::getStatus

# tidy_get_status

(PHP 5, PHP 7, PHP 8, PECL tidy = 0.5.2)

tidy::getStatus -- tidy_get_status — Отримує статус вказаного
документа

### Опис

Об'єктно-орієнтований стиль

public **tidy::getStatus**(): int

Процедурний стиль

**tidy_get_status**([tidy](class.tidy.md) `$tidy`): int

Повертає статус вказаного tidy-об'єкта `tidy`.

### Список параметрів

`tidy`
Об'єкт [Tidy](class.tidy.md).

### Значення, що повертаються

Повертає 0, якщо не було помилок/попереджень, 1 – для попереджень
або можливі помилки або 2 - для помилок.

### Приклади

**Приклад #1 Приклад використання **tidy::getStatus()****

` <?php$html = '<p>параграф</i>';$tidy = new tidy();$tidy->parseString($html);$tidy2 = new tidy();$html2 = '<bogus >тест</bogus>';$tidy2->parseString($html2);echo $tidy->getStatus(); //1echo $tidy2->getStatus(); //2?> `
