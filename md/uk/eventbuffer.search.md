Сканує буфер на наявність рядка

-   [« EventBuffer::readLine](eventbuffer.readline.html)
    
-   [EventBuffer::searchEol »](eventbuffer.searcheol.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Сканує буфер на наявність рядка
    

# EventBuffer::search

(PECL event >= 1.2.6-beta)

EventBuffer::search — Сканує буфер на наявність рядка

### Опис

```methodsynopsis
public
   EventBuffer::search(
    string
     $what
   , 
    int
     $start
     = -1
   , 
    int
     $end
     = -1
   ): mixed
```

Сканує буфер на наявність рядка `what`. Повертає числову позицію рядка або **`false`**, якщо рядок не було знайдено.

Якщо вказано аргумент `start`, він вказує на позицію, з якої має починатися пошук; інакше пошук виконується з початку рядка. Якщо вказано аргумент `end`, пошук виконується між початковою та кінцевою позиціями буфера.

### Список параметрів

`what`

Рядок для пошуку.

`start`

Позиція початку пошуку.

`end`

Позиція закінчення пошуку.

### Значення, що повертаються

Повертає числову позицію першого входження рядка у буфері або **`false`**, якщо рядок не знайдено.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання **EventBuffer::search()****

```php
<?php
// Count total occurances of 'str' in 'buf'
function count_instances($buf, $str) {
    $total = 0;
    $p     = 0;
    $i     = 0;

    while (1) {
        $p = $buf->search($str, $p);
        if ($p === FALSE) {
            break;
        }
        ++$total;
        ++$p;
    }

    return $total;
}

$buf = new EventBuffer();
$buf->add("Some string within a string inside another string");
var_dump(count_instances($buf, "str"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
```

### Дивіться також

-   [EventBuffer::searchEol()](eventbuffer.searcheol.html) - Сканує буфер на наявність кінця рядка