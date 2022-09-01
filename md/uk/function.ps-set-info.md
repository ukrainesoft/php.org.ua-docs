---
navigation:
  - function.ps-set-border-style.html: «pssetborderstyle
  - function.ps-set-parameter.html: псsetparameter »
  - index.html: PHP Manual
  - ref.ps.html: Функції PS
title: псsetinfo
---
# псsetinfo

(PECL ps >= 1.1.0)

псsetinfo — Встановлює інформаційні поля документа

### Опис

```methodsynopsis
ps_set_info(resource $p, string $key, string $val): bool
```

Встановлює певні інформаційні поля документа. Ці поля відображатимуться як коментар у заголовку файлу PostScript. Якщо документ конвертується у PDF, ці поля також будуть використовуватися для інформації про документ.

Для `BoundingBox` зазвичай встановлюється значення, яке присвоєно першій сторінці. Це працює тільки якщо [псfindfont()](function.ps-findfont.html) не викликалася раніше. У таких випадках BoundingBox не буде встановлений, якщо ви не встановите його за допомогою цієї функції.

Функція більше не працюватиме, якщо заголовок файлу postscript вже записаний. Вона повинна викликатись перед першою сторінкою або першим викликом [псfindfont()](function.ps-findfont.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

`key`

Ім'я інформаційного поля, що настроюється. Можна встановити такі значення: `Keywords` `Subject` `Title` `Creator` `Author` `BoundingBox` і `Orientation`. Майте на увазі, що деякі з них мають значення для перегляду документів PostScript.

`value`

Значення інформаційного поля. Поле `Orientation` може бути встановлено як `Portrait` або `Landscape`. У `BoundingBox` - Це рядок, що складається із чотирьох чисел. Перші два числа – координати лівого нижнього кута сторінки. Останні два числа – координати верхнього правого кута.

> **Зауваження**
> 
> До версії 0.2.6 pslib BoundingBox та Orientation будуть перезаписані функцією [псbeginpage()](function.ps-begin-page.html), якщо функція [псfindfont()](function.ps-findfont.html) не була викликана раніше.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псfindfont()](function.ps-findfont.html) - Завантажує шрифт
-   [псbeginpage()](function.ps-begin-page.html) - Починає нову сторінку
