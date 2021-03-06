- [« Типи ресурсів](url.resources.md)
- [Функції URL»](ref.url.md)

- [PHP Manual](index.md)
- [URL](book.url.md)
- Обумовлені константи

# Зумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути
доступні лише в тому випадку, якщо PHP був зібраний за допомогою цього
модуля або в тому випадку, якщо даний модуль був динамічно завантажений
під час виконання.

Наступні константи доступні для використання з
[parse_url()](function.parse-url.md).

**`PHP_URL_SCHEME`** (int)

**`PHP_URL_HOST`** (int)
Виведення імені з хоста розібраного URL-адреси.

**`PHP_URL_PORT`** (int)
Виведення порту із розібраного URL.

**`PHP_URL_USER`** (int)
Виведення користувача з розібраного URL.

**`PHP_URL_PASS`** (int)
Виведення пароля з розібраного URL.

**`PHP_URL_PATH`** (int)
Виведення шляху із розібраного URL.

**`PHP_URL_QUERY`** (int)
Виведення рядка запиту з розібраного URL-адреси.

**`PHP_URL_FRAGMENT`** (int)
Виведення фрагмента (рядок після символу #) із розібраного URL.

Наступні константи призначені для використання з
[http_build_query()](function.http-build-query.md).

**`PHP_QUERY_RFC1738`** (int)
Кодування виконується відповідно до [» RFC 1738](http://www.faqs.org/rfcs/rfc1738) та типом даних
`application/x-www-form-urlencoded`. Це означає, що прогалини
замінюються символом плюс (`+`).

**`PHP_QUERY_RFC3986`** (int)
Кодування здійснюється відповідно до [»RFC 3986](http://www.faqs.org/rfcs/rfc3986), і пробіли кодуються як `% 20`.
