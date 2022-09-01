---
navigation:
  - function.ps-findfont.html: «psfindfont
  - function.ps-get-parameter.html: псgetparameter »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псgetbuffer
---
# псgetbuffer

(PECL ps >= 1.1.0)

псgetbuffer — Отримує повний буфер, що містить PS

### Опис

```methodsynopsis
ps_get_buffer(resource $psdoc): string
```

Функція поки що не реалізована. Вона завжди повертатиме порожній рядок. Ідея для пізнішої реалізації полягає в тому, щоб записати вміст файлу postscript у внутрішній буфер, якщо потрібно створення пам'яті, і отримати вміст буфера за допомогою цієї функції. В даний час документи, створені в пам'яті, надсилаються до браузера без буферизації.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

### Дивіться також

-   [псopenfile()](function.ps-open-file.html) - Відкриває файл для виводу
