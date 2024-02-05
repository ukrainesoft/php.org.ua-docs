---
navigation:
  - class.gender.md: « Gender\\Gender
  - gender-gender.construct.md: 'Gender\\Gender::\_\_construct »'
  - index.md: PHP Manual
  - class.gender.md: Gender\\Gender
title: 'Gender\\Gender::connect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gender\\Gender::connect

(PECL gender >= 0.6.0)

Gender\\Gender::connect — З'єднання із зовнішньою базою імен

### Опис

```methodsynopsis
public Gender\Gender::connect(string $dsn): bool
```

Підключення до зовнішнього словника імен. На даний момент підтримуються лише потокові ресурси.

### Список параметрів

`dsn`

DSN для відкриття.

### Значення, що повертаються

\*\*`true`**либо**`false`\*\*в зависимости от успешности.
