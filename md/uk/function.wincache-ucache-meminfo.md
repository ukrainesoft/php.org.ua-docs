- [«wincache_ucache_info](function.wincache-ucache-info.md)
- [wincache_ucache_set »](function.wincache-ucache-set.md)

- [PHP Manual](index.md)
- [Функції WinCache](ref.wincache.md)
- Отримує інформацію про використання пам'яті кешу користувача

#wincache_ucache_meminfo

(PECL wincache \>= 1.1.0)

wincache_ucache_meminfo — Отримує інформацію про використання пам'яті
кешу користувача

### Опис

**wincache_ucache_meminfo**(): array\|false

Отримує інформацію про використання пам'яті кешу користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання пам'яті користувача кешу або
**`false`** у разі виникнення помилки

Масив, що повертається цією функцією, містить такі елементи:

- `memory_total` - обсяг пам'яті в байтах, виділений для
кешу користувача
- `memory_free` - обсяг вільної пам'яті в байтах, доступної для
кешу користувача
- `num_used_blks` - кількість блоків пам'яті, що використовуються
кешем користувача
- `num_free_blks` - кількість вільних блоків пам'яті, доступних для
кешу користувача
- `memory_overhead` - обсяг пам'яті в байтах, що використовується для
внутрішніх структур кешу користувача

### Приклади

**Приклад #1 Приклад використання **wincache_ucache_meminfo()****

` <pre><?phpprint_r(wincache_ucache_meminfo());?></pre>`

Результат виконання цього прикладу:

Array
(
[memory_total] => 5242880
[memory_free] => 5215056
[num_used_blks] => 6
[num_free_blks] => 3
[memory_overhead] => 176
)

### Дивіться також

- [wincache_fcache_fileinfo()](function.wincache-fcache-fileinfo.md) -
Отримує інформацію про файли, закешовані у файловому кеші
- [wincache_fcache_meminfo()](function.wincache-fcache-meminfo.md) -
Отримує інформацію про використання пам'яті файлового кешу
- [wincache_ocache_fileinfo()](function.wincache-ocache-fileinfo.md) -
Отримує інформацію про файли, закешовані в кеші опкодів
- [wincache_rplist_fileinfo()](function.wincache-rplist-fileinfo.md) -
Отримує інформацію про роздільну здатність кеша шляху до файлу роздільної здатності
- [wincache_rplist_meminfo()](function.wincache-rplist-meminfo.md) -
Отримує інформацію про використання пам'яті за допомогою кеша шляху
файлу дозволу
- [wincache_refresh_if_changed()](function.wincache-refresh-if-changed.md) -
Оновлює записи кеша для закешованих файлів
- [wincache_ucache_info()](function.wincache-ucache-info.md) -
Отримує інформацію про дані, що зберігаються в кеші користувача
- [wincache_scache_info()](function.wincache-scache-info.md) -
Отримує інформацію про файли, закешовані в кеші сесії
- [wincache_scache_meminfo()](function.wincache-scache-meminfo.md) -
Отримує інформацію про використання кеш-пам'яті сесії
