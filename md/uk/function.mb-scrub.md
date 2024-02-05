---
navigation:
  - function.mb-regex-set-options.md: « mb\_regex\_set\_options
  - function.mb-send-mail.md: mb\_send\_mail »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_scrub
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_scrub

(PHP 7 >= 7.2.0, PHP 8)

mb\_scrub — Замінює неправильно сформовані послідовності байтів символом-замінником

### Опис

```methodsynopsis
mb_scrub(string $string, ?string $encoding = null): string
```

Перетворює набір символів із заданого кодування або кодування за замовчуванням, якщо кодування не було вказано, на те саме кодування. Це замінює всі неприпустимі послідовності байтів символом, що замінює.

### Список параметрів

`string`

Вхідний рядок.

`encoding`

Кодировка для интерпретации параметра`string`. Якщо значення опущено або дорівнює **`null`**, буде використано значення директиви [mbstring.internal\_encoding](mbstring.configuration.md#ini.mbstring.internal-encoding), якщо вона встановлена, інакше буде використано значення директиви [default\_charset](ini.core.md#ini.default-charset)

### Значення, що повертаються

Повертає результат у вигляді рядка (string) із заміненими неприпустимими послідовностями байтів.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |
