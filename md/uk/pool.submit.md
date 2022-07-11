- [« Pool::shutdown](pool.shutdown.md)
- [Pool::submitTo »](pool.submitTo.md)

- [PHP Manual](index.md)
- [Pool](class.pool.md)
- Відправляє об'єкт на виконання

# Pool::submit

(PECL pthreads \>= 2.0.0)

Pool::submit — Відправляє об'єкт на виконання

### Опис

public **Pool::submit**([Threaded](class.threaded.md) `$task`): int

Відправляє завдання наступному воркеру в пулі

### Список параметрів

`task`
Завдання для виконання

### Значення, що повертаються

Ідентифікатор воркера, що виконує об'єкт

### Приклади

**Приклад #1 Надсилання завдань**

` <?phpclass MyWork extends Threaded {    public function run() {        /* ... */    }}class MyWorker extends Worker {    public function __construct(Something $something) {        $this->something = $something; }    public function run() {        /** ... **/    }}$pool = new Pool(8, \MyWorker::class, [new Some| );var_dump($pool);?> `

Результат виконання цього прикладу:

object(Pool)#1 (6) {
["size":protected]=>
int(8)
["class":protected]=>
string(8) "MyWorker"
["workers":protected]=>
array(1) {
[0]=>
object(MyWorker)#4 (1) {
["something"]=>
object(Something)#5 (0) {
}
}
}
["work":protected]=>
array(1) {
[0]=>
object(MyWork)#3 (1) {
["worker"]=>
object(MyWorker)#5 (1) {
["something"]=>
object(Something)#6 (0) {
}
}
}
}
["ctor":protected]=>
array(1) {
[0]=>
object(Something)#2 (0) {
}
}
["last":protected]=>
int(1)
}
