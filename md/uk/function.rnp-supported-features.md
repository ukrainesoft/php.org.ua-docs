---
navigation:
  - function.rnp-save-keys.md: « rnp\_save\_keys
  - function.rnp-version-string-full.md: rnp\_version\_string\_full »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_supported\_features
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_supported\_features

(PECL rnp >= 0.1.1)

rnp\_supported\_features — Отримує підтримувані функції у форматі JSON

### Опис

```methodsynopsis
rnp_supported_features(string $type): string|false
```

Отримання рядка у форматі JSON, що містить масив підтримуваних значень ознак rnp (алгоритмів, кривих тощо) за типами.

### Список параметрів

`type`

Підтримувані значення дивіться у константах RNP\_FEATURE\_\*

### Значення, що повертаються

Повертає рядок, що містить JSON-форматований масив алгоритмів, кривих і т.д. або \*\*`false`\*\*в случае возникновения ошибки.
