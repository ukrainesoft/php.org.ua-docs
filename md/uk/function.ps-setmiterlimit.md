---
navigation:
  - function.ps-setlinewidth.md: « ps\_setlinewidth
  - function.ps-setoverprintmode.md: ps\_setoverprintmode »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setmiterlimit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setmiterlimit

(PECL ps >= 1.1.0)

ps\_setmiterlimit - Встановлює межу скосу

### Опис

```methodsynopsis
ps_setmiterlimit(resource $psdoc, float $value): bool
```

Если две линии соединяются под небольшим углом, а для соединения линий установлено значение`PS_LINEJOIN_MITER`, То результуючий виступ буде дуже довгим. Межа скосу - це максимальне співвідношення довжини скосу (довжини виступу) та ширини лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`value`

Максимальне співвідношення між довжиною скосу та шириною лінії. Великі значення (> 10) призведуть до дуже довгих виступів, якщо дві лінії перетинаються під невеликим кутом. Залишіть значення за промовчанням, якщо ви не впевнені, що робите.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_setlinecap()](function.ps-setlinecap.md) \- Встановлює зовнішній вигляд закінчення лінії
-   [ps\_setlinejoin()](function.ps-setlinejoin.md) \- Встановлює спосіб з'єднання ліній
-   [ps\_setlinewidth()](function.ps-setlinewidth.md) \- Встановлює ширину лінії
