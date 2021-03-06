- [«Pool](class.pool.md)
- [Pool::\_\_construct »](pool.construct.md)

- [PHP Manual](index.md)
- [Pool](class.pool.md)
- Збирає посилання на виконані завдання

# Pool::collect

(PECL pthreads \>= 2.0.0)

Pool::collect — Збирає посилання на виконані завдання

### Опис

public **Pool::collect**([Callable](language.types.callable.md)
`$collector` = ?): int

Дозволяє пулу збирати посилання, визначені як сміття додатковим
збирачем.

### Список параметрів

`collector`
Callback-функція збирача, яка повертає логічне значення,
що вказує, чи може завдання бути зібрана чи ні. Тільки в рідкісних
у випадках може знадобитися спеціальний збирач.

### Значення, що повертаються

Кількість завдань, що залишилися в пулі, які потрібно зібрати.

### Список змін

| Версія | Опис                                                                      |
|--------|---------------------------------------------------------------------------|
| v3     | Тепер повертається ціле число, а параметр collector тепер необов'язковий. |

### Приклади

**Приклад #1 Простий приклад використання **Pool::collect()****

` <?php$pool = new Pool(4);for ($i = 0; $i < 15; ++$i) {    $pool->submit(new class extends Threaded {});}wh ->collect()); // до тех пор, поки все завдання не закінчать виконання$pool->shutdown(); `
