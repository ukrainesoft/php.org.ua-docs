- [«EventBuffer::readLine](eventbuffer.readline.md)
- [EventBuffer::searchEol »](eventbuffer.searcheol.md)

- [PHP Manual](index.md)
- [EventBuffer](class.eventbuffer.md)
- Сканує буфер на наявність рядка

# EventBuffer::search

(PECL event \>= 1.2.6-beta)

EventBuffer::search — Сканує буфер на наявність рядка

### Опис

public **EventBuffer::search**( string `$what` , int `$start` = -1 , int
$end = -1):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Сканує буфер на наявність рядка `what`. Повертає числову позицію
рядки або **`false`**, якщо рядок не було знайдено.

Якщо вказано аргумент `start`, він вказує на позицію, з якою повинен
розпочинатися пошук; інакше пошук виконується з початку рядка.
Якщо вказано аргумент `end`, пошук виконується між початковою та кінцевою
позиціями буфера.

### Список параметрів

`what`
Рядок для пошуку.

`start`
Позиція початку пошуку.

`end`
Позиція закінчення пошуку.

### Значення, що повертаються

Повертає числову позицію першого входження рядка у буфері або
**`false`**, якщо рядок не знайдено.

**Увага**

Ця функція може повертати як логічне значення **`false`**, так і
значення не типу boolean, яке наводиться до **`false`**. Більше
Детальну інформацію див. у розділі [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення,
повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання **EventBuffer::search()****

` <?php// Count total occurances of 'str' in 'buf'function count_instances($buf, $str) {    $total = 0; $p    ==0; $i     = 0; while(1) {       |$p = $buf->search($str, $p); if ($p === FALSE) {            break; }        ++$total; ++$p; }   return $total;}$buf = new EventBuffer();$buf->add("Some string within a string inside another string");var_dump(count_instances($buf, )"

Результатом виконання цього прикладу буде щось подібне:

int(3)

### Дивіться також

- [EventBuffer::searchEol()](eventbuffer.searcheol.md) - Сканує
буфер на наявність кінця рядка
