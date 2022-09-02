---
navigation:
  - eventbuffer.search.md: '« EventBuffer::search'
  - eventbuffer.substr.md: 'EventBuffer::substr »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::searchEol'
---
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

Одна з [EventBuffer:EOLконстант](class.eventbuffer.md#eventbuffer.constants)

### Значення, що повертаються

Повертає числову позицію першого входження символу кінця рядка у буфері або \*\*`false`\*\*якщо не знайдено.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Дивіться також

-   [EventBuffer::search()](eventbuffer.search.md) - Сканує буфер на наявність рядка
