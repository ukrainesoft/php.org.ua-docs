---
navigation:
  - url.resources.md: « Типи ресурсів
  - ref.url.md: Опції URL »
  - index.md: PHP Manual
  - book.url.md: URL
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

Наступні константи доступні для використання з [parse\_url()](function.parse-url.md)

**`PHP_URL_SCHEME`**(int)

**`PHP_URL_HOST`**(int)

Вивод імені з хоста розібраного URL.

**`PHP_URL_PORT`**(int)

Виведення порту із розібраного URL.

**`PHP_URL_USER`**(int)

Виведення користувача з розібраного URL.

**`PHP_URL_PASS`**(int)

Виведення пароля із розібраного URL.

**`PHP_URL_PATH`**(int)

Виведення шляху із розібраного URL.

**`PHP_URL_QUERY`**(int)

Виведення рядка запиту з розібраної URL-адреси.

**`PHP_URL_FRAGMENT`**(int)

Виведення фрагмента (рядок після символу #) із розібраного URL.

Наступні константи призначені для використання з [http\_build\_query()](function.http-build-query.md)

**`PHP_QUERY_RFC1738`**(int)

Кодування виконується відповідно до [» RFC 1738](http://www.faqs.org/rfcs/rfc1738) та типом даних `application/x-www-form-urlencoded`. Це означає, що пропуски замінюються символом плюс (`+`

**`PHP_QUERY_RFC3986`**(int)

Кодування здійснюється відповідно до [» RFC 3986](http://www.faqs.org/rfcs/rfc3986), і пробіли кодуються як `%20`
