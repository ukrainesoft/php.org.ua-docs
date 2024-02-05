---
navigation:
  - function.rpminfo.md: « rpminfo
  - book.xlswriter.md: XLSWriter »
  - index.md: PHP Manual
  - ref.rpminfo.md: Функції RpmInfo
title: rpmvercmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rpmvercmp

(PECL rpminfo >= 0.1.0)

rpmvercmp — Порівняє версії RPM

### Опис

```methodsynopsis
rpmvercmp(string $evr1, string $evr2, ?string $operator = null): int|bool
```

Порівнює версії двох RPM.

### Список параметрів

`evr1`

Перша версія у форматі epoch:version-release

`evr2`

Друга версія у форматі epoch:version-release

`operator`

Необов'язковий оператор. Доступні оператори: `<` `lt` `<=` `le` `>` `gt` `>=` `ge` `==` `=` `eq` `!=` `<>` `ne`соответственно.

Цей параметр чутливий до регістру, значення необхідно вказувати у нижньому регістрі.

### Значення, що повертаються

Повертає < 0, якщо evr1 менше evr2, > 0, якщо evr1 більше evr2 і 0, якщо вони ідентичні.

Якщо буде отримано необов'язковий параметр `operator` функція поверне **`true`**, якщо порівняння відповідатиме тому, що задано оператором, інакше **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 0.7.0 | Було додано необов'язковий аргумент `operator` |
