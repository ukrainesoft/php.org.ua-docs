---
navigation:
  - function.ps-setflat.md: « ps\_setflat
  - function.ps-setgray.md: ps\_setgray »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setfont
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setfont

(PECL ps >= 1.1.0)

ps\_setfont — Встановлює шрифт, який використовуватиметься для наступного виводу

### Опис

```methodsynopsis
ps_setfont(resource $psdoc, int $fontid, float $size): bool
```

Встановлює шрифт, який має бути завантажений раніше за допомогою [ps\_findfont()](function.ps-findfont.md). Виведення тексту без встановлення шрифту призводить до помилки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`fontid`

Ідентифікатор шрифту, повернутий [ps\_findfont()](function.ps-findfont.md)

`size`

Розмір шрифту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_findfont()](function.ps-findfont.md) \- Завантажує шрифт
-   [ps\_set\_text\_pos()](function.ps-set-text-pos.md) \- Встановлює позицію для виведення тексту на приклад.
