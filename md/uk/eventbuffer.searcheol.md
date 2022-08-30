Сканує буфер на наявність кінця рядка

-   [« EventBuffer::search](eventbuffer.search.html)
    
-   [EventBuffer::substr »](eventbuffer.substr.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Сканує буфер на наявність кінця рядка
    

# EventBuffer::searchEol

(PECL event >= 1.5.0)

EventBuffer::searchEol — Сканує буфер на наявність кінця рядка

### Опис

```methodsynopsis
public
   EventBuffer::searchEol(
    int
     $start
     = -1
   , 
    int
     $eol_style
     = 
     EventBuffer::EOL_ANY
    
   ): mixed
```

Сканує буфер на наявність кінця рядка, вказаного параметром `eol_style`. Повертає числову позицію рядка або **`false`**, якщо рядок не було знайдено.

Якщо вказано аргумент `start`, Він представляє позицію, з якої повинен починатися пошук; інакше пошук виконується з початку рядка. Якщо вказано аргумент `end`, пошук виконується між початковою та кінцевою позиціями буфера.

### Список параметрів

`start`

Start search position.

`eol_style`

Одна з [EventBuffer:EOLконстант](class.eventbuffer.html#eventbuffer.constants)

### Значення, що повертаються

Повертає числову позицію першого входження символу кінця рядка у буфері або \*\*`false`\*\*якщо не знайдено.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Дивіться також

-   [EventBuffer::search()](eventbuffer.search.html) - Сканує буфер на наявність рядка