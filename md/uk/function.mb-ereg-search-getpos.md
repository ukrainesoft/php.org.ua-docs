Повертає початкову позицію наступного збігу з регулярним виразом

-   [« mberegreplace](function.mb-ereg-replace.html)
    
-   [мбeregsearchgetregs »](function.mb-ereg-search-getregs.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
    
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

**мбeregsearchgetpos()** повертає початкову позицію наступного збігу з регулярним виразом для функцій [мбeregsearch()](function.mb-ereg-search.html) [мбeregsearchpos()](function.mb-ereg-search-pos.html) [мбeregsearchregs()](function.mb-ereg-search-regs.html). Позиція представляється як числа байт з початку рядка.

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.html)

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.html) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбeregsearchsetpos()](function.mb-ereg-search-setpos.html) - Задає початкову позицію у рядку, з якого розпочнеться пошук відповідностей регулярному виразу