---
navigation:
  - xml.setup.html: « Встановлення та налаштування
  - xml.installation.html: Установка »
  - index.html: PHP Manual
  - xml.setup.html: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Для коректної роботи цього модуля потрібний PHP-модуль [libxml](book.libxml.html). Це означає, що також потрібна передача опції **\-with-libxml**, або до PHP 7.4 **\-enable-libxml**, хоча це вже неявно зроблено, оскільки підтримка libxml за замовчуванням включена.

Модуль використовує expatсумісний шар за промовчанням. Також може бути використаний expat, який може бути знайдений тут: [» http://www.jclark.com/xml/expat.html](http://www.jclark.com/xml/expat.html). Makefile, що поставляється з expat не створює бібліотеку за замовчуванням, ви можете використовувати таке правило для цього:

libexpat.a: $(OBJS) ar -rc $@$(OBJS) ranlib $@

Вихідний пакет RPM expat може бути знайдений тут:[» http://sourceforge.net/projects/expat/](http://sourceforge.net/projects/expat/)
