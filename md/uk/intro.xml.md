---
navigation:
  - book.xml.md: « Розбір XML
  - xml.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.xml.md: Розбір XML
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

XML (eXtensible Markup Language - мова розмітки, що розширюється) - це формат даних для обміну структурованими документами у всесвітній мережі. Цей стандарт визначено Консорціумом Всесвітньої павутини (W3C). Інформація про XML та пов'язані технології може бути знайдена на [» http://www.w3.org/XML/](http://www.w3.org/XML/)

Цей модуль PHP реалізує підтримку бібліотеки expat Джеймса Кларка в PHP. Даний інструментарій дозволяє розбирати, але не перевіряти XML-документи. Він підтримує три [кодування символів](xml.encoding.md) вихідного тексту також підтримуваних PHP: `US-ASCII` `ISO-8859-1`и`UTF-8`. . `UTF-16` не підтримується.

Модуль позволит вам[створювати XML-аналізатори](function.xml-parser-create.md) і далі визначити *обробники* для різних подій. Кожен XML-аналізатор також має декілька [параметрів](function.xml-parser-set-option.md)Ви можете налаштувати.
