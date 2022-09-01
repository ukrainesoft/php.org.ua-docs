---
navigation:
  - iconv.resources.md: « Типи ресурсів
  - ref.iconv.md: Функции iconv »
  - index.md: PHP Manual
  - book.iconv.md: iconv
title: Обумовлені константи
---
# Обумовлені константи

Можливо дізнатися під час виконання, яка реалізація `iconv` використовується модулем.

**Константи реалізації `iconv`**

| Имя | Тип | Описание |
| --- | --- | --- |
| **`ICONV_IMPL`** | string | Реалізація |
| **`ICONV_VERSION`** | string | Версія реалізації |

> **Зауваження**
> 
> Використовуйте ці константи для написання сценаріїв, незалежних від реалізації.

Доступні також такі константи:

**Інші константи `iconv`**

| Имя | Тип | Описание |
| --- | --- | --- |
| **`ICONV_MIME_DECODE_STRICT`** | int | Бітова маска, що використовується в [iconvmimedecode()](function.iconv-mime-decode.html) |
| **`ICONV_MIME_DECODE_CONTINUE_ON_ERROR`** | int | Бітова маска, що використовується в [iconvmimedecode()](function.iconv-mime-decode.html) |
