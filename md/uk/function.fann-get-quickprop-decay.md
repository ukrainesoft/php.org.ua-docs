---
navigation:
  - function.fann-get-num-output.md: « fann\_get\_num\_output
  - function.fann-get-quickprop-mu.md: fann\_get\_quickprop\_mu »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_quickprop\_decay
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_quickprop\_decay

(PECL fann >= 1.0.0)

fann\_get\_quickprop\_decay — Повертає зниження, яке є фактором, при якому ваги повинні зменшуватись на кожній ітерації під час навчання quickprop

### Опис

```methodsynopsis
fann_get_quickprop_decay(resource $ann): float
```

Зниження - це невелике число з негативними значеннями, яке є фактором, за яким ваги повинні зменшуватися на кожній ітерації під час навчання quickprop. Використовується для того, щоб під час навчання ваги не ставали надто високими.

The default decay is -0.0001.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Снижение или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_quickprop\_decay()](function.fann-set-quickprop-decay.md) \- Встановлює коефіцієнт загасання quickprop
