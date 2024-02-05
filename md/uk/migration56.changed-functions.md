---
navigation:
  - migration56.deprecated.md: '« Функціонал, оголошений застарілим у PHP 5.6.x'
  - migration56.new-functions.md: Нові функції »
  - index.md: PHP Manual
  - migration56.md: Міграція з PHP 5.5.x на PHP 5.6.x
title: Змінені функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Змінені функції

### Ядро PHP

-   [crypt()](function.crypt.md)тепер генерує попередження\*\*`E_NOTICE`\*\*, якщо параметр `salt`опущений.
-   [substr\_compare()](function.substr-compare.md)тепер приймає в качестве значения параметра`length`
-   [unserialize()](function.unserialize.md)тепер зазнає невдачі, якщо передано серіалізовані дані, які були змінені у спробі інстанціювати об'єкт без виклику його конструктора.

### [cURL](book.curl.md)

-   Завантаження на сервер із використанням синтаксису`@file`тепер підтримується, тільки якщо опція\*\*`CURLOPT_SAFE_UPLOAD`**установлена в**`false`\*\*. Натомість слід користуватися[CURLFile](class.curlfile.md)

### [Mcrypt](book.mcrypt.md)

-   Параметр`source` функції [mcrypt\_create\_iv()](function.mcrypt-create-iv.md)тепер має значення за умовчанням\*\*`MCRYPT_DEV_URANDOM`\*\* замість **`MCRYPT_DEV_RANDOM`**

### [OpenSSL](book.openssl.md)

-   [stream\_socket\_enable\_crypto()](function.stream-socket-enable-crypto.md)тепер дозволяє не вказувати параметр`crypto_type`якщо контекст потоку SSL включає нову опцію`crypto_type`

### [PostgreSQL](book.pgsql.md)

-   [pg\_insert()](function.pg-insert.md) [pg\_select()](function.pg-select.md) [pg\_update()](function.pg-update.md) і [pg\_delete()](function.pg-delete.md)більше не є експериментальними.
-   [pg\_send\_execute()](function.pg-send-execute.md) [pg\_send\_prepare()](function.pg-send-prepare.md) [pg\_send\_query()](function.pg-send-query.md) і [pg\_send\_query\_params()](function.pg-send-query-params.md)більше не блокуються до завершення запису запиту, якщо нижчий потік сокету для з'єднання з базою даних перебуває в режимі неблокування.

### [Reflection](book.reflection.md)

-   [ReflectionClass::newInstanceWithoutConstructor()](reflectionclass.newinstancewithoutconstructor.md)тепер дозволяє створювати екземпляри із неостаточних (non-final) внутрішніх класів.

### [XMLReader](book.xmlreader.md)

-   [XMLReader::getAttributeNs()](xmlreader.getattributens.md) і [XMLReader::getAttributeNo()](xmlreader.getattributeno.md)тепер повертають\*\*`null`\*\*якщо атрибут не може бути знайдений, як це робить[XMLReader::getAttribute()](xmlreader.getattribute.md)
