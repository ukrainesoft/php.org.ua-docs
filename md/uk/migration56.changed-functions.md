---
navigation:
  - migration56.deprecated.md: '« Функціонал, оголошений застарілим у PHP 5.6.x'
  - migration56.new-functions.html: Нові функції »
  - index.md: PHP Manual
  - migration56.md: Миграция с PHP 5.5.x на PHP 5.6.x
title: Змінені функції
---
## Змінені функції

### Ядро PHP

-   [crypt()](function.crypt.md) тепер генерує попередження **`E_NOTICE`**, якщо параметр `salt` опущений.
-   [substrcompare()](function.substr-compare.md) тепер приймає `0` як значення параметра `length`
-   [unserialize()](function.unserialize.md) тепер зазнає невдачі, якщо передано серіалізовані дані, які були змінені у спробі інстанціювати об'єкт без виклику його конструктора.

### [cURL](book.curl.md)

-   Завантаження на сервер із використанням синтаксису `@file` тепер підтримується, тільки якщо опція **`CURLOPT_SAFE_UPLOAD`** встановлена ​​в **`false`**. Натомість слід користуватися [CURLFile](class.curlfile.md)

### [Mcrypt](book.mcrypt.md)

-   Параметр `source` функції [mcryptcreateiv()](function.mcrypt-create-iv.md) тепер має значення за умовчанням **`MCRYPT_DEV_URANDOM`** замість **`MCRYPT_DEV_RANDOM`**

### [OpenSSL](book.openssl.md)

-   [streamsocketenablecrypto()](function.stream-socket-enable-crypto.md) тепер дозволяє не вказувати параметр `crypto_type`якщо контекст потоку SSL включає нову опцію `crypto_type`

### [PostgreSQL](book.pgsql.md)

-   [пгinsert()](function.pg-insert.html) [пгselect()](function.pg-select.html) [пгupdate()](function.pg-update.html) і [пгdelete()](function.pg-delete.md) більше не є експериментальними.
-   [пгsendexecute()](function.pg-send-execute.html) [пгsendprepare()](function.pg-send-prepare.html) [пгsendquery()](function.pg-send-query.html) і [пгsendqueryparams()](function.pg-send-query-params.md) більше не блокуються до завершення запису запиту, якщо нижчий потік сокету для з'єднання з базою даних перебуває в режимі неблокування.

### [Reflection](book.reflection.md)

-   [ReflectionClass::newInstanceWithoutConstructor()](reflectionclass.newinstancewithoutconstructor.md) тепер дозволяє створювати екземпляри із неостаточних (non-final) внутрішніх класів.

### [XMLReader](book.xmlreader.md)

-   [XMLReader::getAttributeNs()](xmlreader.getattributens.md) і [XMLReader::getAttributeNo()](xmlreader.getattributeno.md) тепер повертають \*\*`null`\*\*якщо атрибут не може бути знайдений, як це робить [XMLReader::getAttribute()](xmlreader.getattribute.md)
