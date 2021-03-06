- [«headers_sent](function.headers-sent.md)
- [inet_ntop »](function.inet-ntop.md)

- [PHP Manual](index.md)
- [Мережні функції](ref.network.md)
- Отримує чи встановлює код відповіді HTTP

# http_response_code

(PHP 5 \>= 5.4.0, PHP 7, PHP 8)

http_response_code — Отримує або встановлює код відповіді HTTP

### Опис

**http_response_code**(int `$response_code` = 0): int\|bool

Отримує або визначає коди відповідей HTTP.

### Список параметрів

`response_code`
Код відповіді встановлюється за допомогою опціонального параметра
`response_code`.

### Значення, що повертаються

Якщо `response_code` заданий, буде повернено попередній код статусу.
Якщо `response_code` не заданий, буде повернено поточний код статусу.
Обидва ці значення будуть за промовчанням мати код стану `200`, якщо вони
використовуються в оточенні веб-сервера.

Якщо `response_code` не заданий та використовується не в оточенні веб-сервера
(наприклад, у CLI), то буде повернено **`false`**. Якщо `response_code`
заданий та використовується не в оточенні веб-сервера, то буде повернено
**`true`** (але якщо не було встановлено попереднього коду статусу).

### Приклади

**Приклад #1 Використання **http_response_code()** в оточенні
веб-сервера**

` <?php// Беремо поточний код і встановлюємо новийvar_dump(http_response_code(404));// Беремо новий кодvar_dump(http_response_code());?> `

Результат виконання цього прикладу:

int(200)
int(404)

**Приклад #2 Використання **http_response_code()** у CLI**

` <?php// Беремо поточний код по замовчуваннямvar_dump(http_response_code());// Встановлюємо кодvar_dump(http_response_code(201));// Беремо новий кодvar_dump(?

Результат виконання цього прикладу:

bool(false)
bool(true)
int(201)

### Дивіться також

- [header()](function.header.md) - Надсилання HTTP-заголовка
- [headers_list()](function.headers-list.md) - Повертає список
переданих заголовків (або готових до відправлення)
