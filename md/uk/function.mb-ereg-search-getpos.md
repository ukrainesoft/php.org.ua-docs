Повертає початкову позицію наступного збігу з регулярним виразом

-   [« mb\_ereg\_replace](function.mb-ereg-replace.html)
    
-   [mb\_ereg\_search\_getregs »](function.mb-ereg-search-getregs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Повертає початкову позицію наступного збігу з регулярним виразом
    

# мбeregsearchgetpos

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregsearchgetpos - Повертає початкову позицію наступного збігу з регулярним виразом

### Опис

```methodsynopsis
mb_ereg_search_getpos(): int
```

Повертає початкову позицію наступного збігу з регулярним виразом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**мбeregsearchgetpos()** повертає початкову позицію наступного збігу з регулярним виразом для функцій [mb\_ereg\_search()](function.mb-ereg-search.html) [mb\_ereg\_search\_pos()](function.mb-ereg-search-pos.html) [mb\_ereg\_search\_regs()](function.mb-ereg-search-regs.html). Позиція представляється як числа байт з початку рядка.

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.html)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.html) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [mb\_ereg\_search\_setpos()](function.mb-ereg-search-setpos.html) - Задає початкову позицію у рядку, з якого розпочнеться пошук відповідностей регулярному виразу