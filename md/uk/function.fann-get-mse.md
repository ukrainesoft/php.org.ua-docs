---
navigation:
  - function.fann-get-learning-rate.md: « fann\_get\_learning\_rate
  - function.fann-get-network-type.md: fann\_get\_network\_type »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_MSE
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_MSE

(PECL fann >= 1.0.0)

fann\_get\_MSE — Зчитує середньоквадратичну помилку мережі

### Опис

```methodsynopsis
fann_get_MSE(resource $ann): float
```

Зчитує середньоквадратичну помилку мережі.

Зчитує середньоквадратичну помилку мережі. Це значення обчислюється під час навчання або тестування і тому іноді може трохи відрізнятися, якщо вага була змінена з моменту останнього обчислення значення.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Среднеквадратичная ошибка или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_test\_data()](function.fann-test-data.md) \- Тестування набору навчальних даних та обчислення MSE для нього
