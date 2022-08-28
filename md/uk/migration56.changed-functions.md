Змінені функції

-   [« Функционал, объявленный устаревшим в PHP 5.6.x](migration56.deprecated.html)
    
-   [Новые функции »](migration56.new-functions.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 5.5.x на PHP 5.6.x](migration56.html)
    
-   Змінені функції
    

## Змінені функції

### Ядро PHP

-   [crypt()](function.crypt.html) тепер генерує попередження **`E_NOTICE`**, якщо параметр `salt` опущений.
-   [substr\_compare()](function.substr-compare.html) тепер приймає `0` як значення параметра `length`
-   [unserialize()](function.unserialize.html) тепер зазнає невдачі, якщо передано серіалізовані дані, які були змінені у спробі інстанціювати об'єкт без виклику його конструктора.

### [cURL](book.curl.html)

-   Завантаження на сервер із використанням синтаксису `@file` тепер підтримується, тільки якщо опція **`CURLOPT_SAFE_UPLOAD`** встановлена ​​в **`false`**. Натомість слід користуватися [CURLFile](class.curlfile.html)

### [Mcrypt](book.mcrypt.html)

-   Параметр `source` функції [mcrypt\_create\_iv()](function.mcrypt-create-iv.html) тепер має значення за умовчанням **`MCRYPT_DEV_URANDOM`** замість **`MCRYPT_DEV_RANDOM`**

### [OpenSSL](book.openssl.html)

-   [stream\_socket\_enable\_crypto()](function.stream-socket-enable-crypto.html) тепер дозволяє не вказувати параметр `crypto_type`якщо контекст потоку SSL включає нову опцію `crypto_type`

### [PostgreSQL](book.pgsql.html)

-   [pg\_insert()](function.pg-insert.html) [pg\_select()](function.pg-select.html) [pg\_update()](function.pg-update.html) і [pg\_delete()](function.pg-delete.html) більше не є експериментальними.
-   [pg\_send\_execute()](function.pg-send-execute.html) [pg\_send\_prepare()](function.pg-send-prepare.html) [pg\_send\_query()](function.pg-send-query.html) і [pg\_send\_query\_params()](function.pg-send-query-params.html) більше не блокуються до завершення запису запиту, якщо нижчий потік сокету для з'єднання з базою даних перебуває в режимі неблокування.

### [Reflection](book.reflection.html)

-   [ReflectionClass::newInstanceWithoutConstructor()](reflectionclass.newinstancewithoutconstructor.html) тепер дозволяє створювати екземпляри із неостаточних (non-final) внутрішніх класів.

### [XMLReader](book.xmlreader.html)

-   [XMLReader::getAttributeNs()](xmlreader.getattributens.html) і [XMLReader::getAttributeNo()](xmlreader.getattributeno.html) тепер повертають **`null`**якщо атрибут не може бути знайдений, як це робить [XMLReader::getAttribute()](xmlreader.getattribute.html)