---
navigation:
  - ref.outcontrol.md: « Функції контролю виведення
  - function.ob-clean.md: ob\_clean »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: flush
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# flush

(PHP 4, PHP 5, PHP 7, PHP 8)

flush — Скидає системний буфер виводу

### Опис

```methodsynopsis
flush(): void
```

Скидає системні буфери запису PHP та серверної частини, якою користується PHP (наприклад: CGI, веб-сервер). У командному рядку функція **flush()** спробує скинути лише вміст буферів, тоді як у веб-контексті скидаються заголовки та вміст буферів.

> **Зауваження**: Функция**flush()**, можливо, не зможе перевизначити схему буферизації веб-сервера і робота функція не позначиться на буферизації на стороні клієнта в браузері.

> **Зауваження**: Функція не впливає на обробники виведення рівня користувача, наприклад ті, які запускаються функціями [ob\_start()](function.ob-start.md) або [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md)

**Увага**

Функция**flush()** може заважати обробникам висновку, які встановлюють та надсилають заголовки у веб-контексті (наприклад, функція-обробник [ob\_gzhandler()](function.ob-gzhandler.md)) відправляючи заголовки до того, як обробники зможуть це зробити.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ob\_flush()](function.ob-flush.md) \- Скидає (відправляє) повернене активним обробником висновку значення
-   [ob\_clean()](function.ob-clean.md) \- Очищає (стирає) вміст активного буфера виводу
-   [ob\_end\_flush()](function.ob-end-flush.md) \- Скидає (відправляє) значення активного оброблювача виводу, що повертається, і відключає активний буфер виводу
-   [ob\_end\_clean()](function.ob-end-clean.md) \- Очищає (стирає) вміст активного буфера виведення та відключає його
