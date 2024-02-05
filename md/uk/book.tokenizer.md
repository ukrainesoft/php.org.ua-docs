---
navigation:
  - function.tidy-warning-count.md: « tidy\_warning\_count
  - intro.tokenizer.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.other.md: Інші базові модулі
title: Лексер (Tokenizer)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Лексер (Tokenizer)

-   [Вступ](intro.tokenizer.md)
-   [Встановлення та налаштування](tokenizer.setup.md)
    -   [Вимоги](tokenizer.requirements.md)
    -   [Установка](tokenizer.installation.md)
    -   [Налаштування під час виконання](tokenizer.configuration.md)
    -   [Типи ресурсів](tokenizer.resources.md)
-   [Обумовлені константи](tokenizer.constants.md)
-   [Приклади](tokenizer.examples.md)
-   [PhpToken](class.phptoken.md) \- Клас PhpToken
    -   [PhpToken::\_\_construct](phptoken.construct.md) \- Створює об'єкт PhpToken
    -   [PhpToken::getTokenName](phptoken.gettokenname.md) \- Повертає ім'я токена
    -   [PhpToken::is](phptoken.is.md)— Перевіряє, чи відповідає токен зазначеному типу
    -   [PhpToken::isIgnorable](phptoken.isignorable.md)— Повідомляє, чи токен ігноруватиметься парсером PHP
    -   [PhpToken::\_\_function toString() { \[native code\] }](phptoken.tostring.md)— Повертає текстовий вміст токена
    -   [PhpToken::tokenize](phptoken.tokenize.md)— Розбирає заданий рядок, що містить програму на PHP, масив об'єктів PhpToken
-   [Функції PHP-лексера (tokenizer)](ref.tokenizer.md)
    -   [token\_get\_all](function.token-get-all.md)— Розбиває переданий вихідний код на PHP-лексеми
    -   [token\_name](function.token-name.md)— Отримати символьне ім'я для переданої PHP-лексеми
