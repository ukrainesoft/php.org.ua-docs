---
navigation:
  - iconv.resources.md: « Типи ресурсів
  - ref.iconv.md: Функції iconv »
  - index.md: PHP Manual
  - book.iconv.md: iconv
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Можливо дізнатися під час виконання, яка реалізація `iconv` використовується модулем.

**Константи реалізації `iconv`**

| Имя | Тип | Опис |
| --- | --- | --- |
| **`ICONV_IMPL`** | string | Реалізація |
| **`ICONV_VERSION`** | string | Версія реалізації |

> **Зауваження** :
> 
> Використовуйте ці константи для написання сценаріїв, незалежних від реалізації.

Доступні також такі константи:

**Інші константи `iconv`**

| Имя | Тип | Опис |
| --- | --- | --- |
| **`ICONV_MIME_DECODE_STRICT`** | int | Бітова маска, що використовується в [iconv\_mime\_decode()](function.iconv-mime-decode.md) |
| **`ICONV_MIME_DECODE_CONTINUE_ON_ERROR`** | int | Бітова маска, що використовується в [iconv\_mime\_decode()](function.iconv-mime-decode.md) |
