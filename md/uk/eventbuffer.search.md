---
navigation:
  - eventbuffer.readline.md: '« EventBuffer::readLine'
  - eventbuffer.searcheol.md: 'EventBuffer::searchEol »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::search'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Если указан аргумент`start`, Вказує на позицію, з якої повинен починатися пошук; інакше пошук виконується з початку рядка. Якщо вказано аргумент `end`, пошук виконується між початковою та кінцевою позиціями буфера.

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

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання** EventBuffer::search()\*\*\*\*

```php
<?php
// Count total occurances of 'str' in 'buf'
function count_instances($buf, $str) {
    $total = 0;
    $p     = 0;
    $i     = 0;

    while (1) {
        $p = $buf->search($str, $p);
        if ($p === FALSE) {
            break;
        }
        ++$total;
        ++$p;
    }

    return $total;
}

$buf = new EventBuffer();
$buf->add("Some string within a string inside another string");
var_dump(count_instances($buf, "str"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
```

### Дивіться також

-   [EventBuffer::searchEol()](eventbuffer.searcheol.md) \- Сканує буфер на наявність кінця рядка
