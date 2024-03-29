---
navigation:
  - function.ps-set-border-style.md: « ps\_set\_border\_style
  - function.ps-set-parameter.md: ps\_set\_parameter »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_set\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_set\_info

(PECL ps >= 1.1.0)

ps\_set\_info — Встановлює інформаційні поля документа

### Опис

```methodsynopsis
ps_set_info(resource $p, string $key, string $val): bool
```

Встановлює певні інформаційні поля документа. Ці поля відображатимуться як коментар у заголовку файлу PostScript. Якщо документ конвертується у PDF, ці поля також будуть використовуватися для інформації про документ.

Для`BoundingBox` зазвичай встановлюється значення, яке присвоєно першій сторінці. Це працює тільки якщо [ps\_findfont()](function.ps-findfont.md) не викликалася раніше. У таких випадках BoundingBox не буде встановлений, якщо ви не встановите його за допомогою цієї функції.

Функція більше не працюватиме, якщо заголовок файлу postscript вже записаний. Вона повинна викликатись перед першою сторінкою або першим викликом [ps\_findfont()](function.ps-findfont.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`key`

Ім'я інформаційного поля, що настроюється. Можна встановити такі значення: `Keywords` `Subject` `Title` `Creator` `Author` `BoundingBox`и`Orientation`. Майте на увазі, що деякі з них мають значення для перегляду документів PostScript.

`value`

Значение информационного поля. Поле`Orientation` може бути встановлено як `Portrait`или`Landscape`. `BoundingBox` - Це рядок, що складається із чотирьох чисел. Перші два числа – координати лівого нижнього кута сторінки. Останні два числа – координати верхнього правого кута.

> **Зауваження** :
> 
> До версії 0.2.6 pslib BoundingBox та Orientation будуть перезаписані функцією [ps\_begin\_page()](function.ps-begin-page.md), якщо функція [ps\_findfont()](function.ps-findfont.md) не була викликана раніше.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_findfont()](function.ps-findfont.md) \- Завантажує шрифт
-   [ps\_begin\_page()](function.ps-begin-page.md) \- Починає нову сторінку
