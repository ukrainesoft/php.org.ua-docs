---
navigation:
  - xsl.resources.md: « Типи ресурсів
  - xsl.examples.md: Приклади »
  - index.md: PHP Manual
  - book.xsl.md: XSL
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`XSL_CLONE_AUTO`**(int)

**`XSL_CLONE_NEVER`**(int)

**`XSL_CLONE_ALWAYS`**(int)

**`LIBXSLT_VERSION`**(int)

версія libxslt формату 10117

**`LIBXSLT_DOTTED_VERSION`**(string)

Версія libxslt формату 1.1.17.

**`LIBEXSLT_VERSION`**(int)

версія libexslt формату 813.

**`LIBEXSLT_DOTTED_VERSION`**(string)

Версія libexslt формату 1.1.17.

**`XSL_SECPREF_NONE`**(int)

Вимкнення всіх обмежень безпеки.

**`XSL_SECPREF_READ_FILE`**(int)

Забороняє читати файли.

**`XSL_SECPREF_WRITE_FILE`**(int)

Забороняє записувати файл.

**`XSL_SECPREF_CREATE_DIRECTORY`**(int)

Забороняє створення каталогів.

**`XSL_SECPREF_READ_NETWORK`**(int)

Забороняє читати мережеві файли.

**`XSL_SECPREF_WRITE_NETWORK`**(int)

Забороняє запис мережних файлів.

**`XSL_SECPREF_DEFAULT`**(int)

Забороняє всі види доступу запис, тобто. бітова маска **`XSL_SECPREF_WRITE_NETWORK`** **`XSL_SECPREF_CREATE_DIRECTORY`** **`XSL_SECPREF_WRITE_FILE`**
