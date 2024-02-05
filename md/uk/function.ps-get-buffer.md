---
navigation:
  - function.ps-findfont.md: « ps\_findfont
  - function.ps-get-parameter.md: ps\_get\_parameter »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_get\_buffer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_get\_buffer

(PECL ps >= 1.1.0)

ps\_get\_buffer — Отримує повний буфер, що містить PS

### Опис

```methodsynopsis
ps_get_buffer(resource $psdoc): string
```

Функція поки що не реалізована. Вона завжди повертатиме порожній рядок. Ідея для пізнішої реалізації полягає в тому, щоб записати вміст файлу postscript у внутрішній буфер, якщо потрібно створення пам'яті, і отримати вміст буфера за допомогою цієї функції. В даний час документи, створені в пам'яті, надсилаються до браузера без буферизації.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

### Дивіться також

-   [ps\_open\_file()](function.ps-open-file.md) \- Відкриває файл для виводу
