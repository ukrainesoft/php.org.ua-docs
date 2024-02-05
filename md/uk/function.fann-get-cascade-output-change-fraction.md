---
navigation:
  - function.fann-get-cascade-num-candidates.md: « fann\_get\_cascade\_num\_candidates
  - function.fann-get-cascade-output-stagnation-epochs.md: fann\_get\_cascade\_output\_stagnation\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_output\_change\_fraction
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_output\_change\_fraction

(PECL fann >= 1.0.0)

fann\_get\_cascade\_output\_change\_fraction — Повертає частку зміни виходу каскаду

### Опис

```methodsynopsis
fann_get_cascade_output_change_fraction(resource $ann): float
```

Частка зміни виходу каскаду - це число від 0 до 1, що визначає, наскільки більша частина значення [fann\_get\_MSE()](function.fann-get-mse.md)должна измениться в[fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.md) під час навчання вихідних з'єднань, щоб навчання, щоб не застоювалося. Якщо навчання зупиниться, навчання вихідних з'єднань буде припинено та будуть підготовлені нові кандидати.

Це означає, що якщо MSE не змінюється на частку \*\*fann\_get\_cascade\_output\_change\_fraction()\*\*в течение периода[fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.md), Навчання вихідних з'єднань припиниться, тому що навчання зупинилося.

Якщо частка зміни виходу каскаду мала, вихідні з'єднання навчатимуться більше, і якщо частка висока, вони навчатимуться менше.

Частка зміни виходу каскаду за замовчуванням становить 0.01, що еквівалентно зміни MSE на 1%.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Частка зміни виходу каскаду або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_output\_change\_fraction()](function.fann-set-cascade-output-change-fraction.md) \- Встановлює частку зміни каскадних вихідних даних
-   [fann\_get\_MSE()](function.fann-get-mse.md) \- Зчитує середньоквадратичну помилку мережі
-   [fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.md) \- Повертає кількість каскадних періодів застою кандидатів
