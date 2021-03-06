- [«xdiff](book.xdiff.md)
- [Встановлення та налаштування »](xdiff.setup.md)

- [PHP Manual](index.md)
- [xdiff](book.xdiff.md)
-   Вступ

# Вступ

Модуль xdiff дозволяє створювати та застосовувати файли виправлень,
містять відмінності між різними версіями файлів.

Модуль підтримує два режими роботи: з рядками та з файлами, також,
два різні формати патчів - уніфікований та бінарний. Уніфіковані
патчі хороші для текстових файлів та зручні для читання людиною. Для
бінарних файлів, таких як архіви або зображення, слід використовувати
бінарний формат, оскільки він коректно обробляє недруковані символи.

Починаючи з версії 1.5.0 існують два різні набори функцій для
створення бінарних патчів. Нові функції -
[xdiff_string_rabdiff()](function.xdiff-string-rabdiff.md) та
[xdiff_file_rabdiff()](function.xdiff-file-rabdiff.md) створюють
підтримуваний старими функціями висновок, але швидше і результат
займає менше місця. Докладніше про методи створення бінарних патчів
та різниці між ними читайте на сайті
[» libxdiff](http://www.xmailserver.org/xdiff-lib.md).

Модуль використовує libxdiff. Детальніше читайте на сайті
[»http://www.xmailserver.org/xdiff-lib.md](http://www.xmailserver.org/xdiff-lib.md).
