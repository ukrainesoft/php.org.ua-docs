- [« ArrayObject::\_\_construct](arrayobject.construct.md)
- [ArrayObject::exchangeArray »](arrayobject.exchangearray.md)

- [PHP Manual](index.md)
- [ArrayObject](class.arrayobject.md)
- Отримати кількість загальнодоступних властивостей ArrayObject

# ArrayObject::count

(PHP 5, PHP 7, PHP 8)

ArrayObject::count — Отримати кількість загальнодоступних властивостей
ArrayObject

### Опис

public **ArrayObject::count**(): int

Отримати кількість загальнодоступних властивостей
[ArrayObject](class.arrayobject.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість загальнодоступних властивостей [ArrayObject](class.arrayobject.md).

> **Примітка**:
>
> Якщо [ArrayObject](class.arrayobject.md) створюється із масиву, то
> всі властивості загальнодоступні.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::count()****

'third'));var_dump($arrayobj->count());?> `` <?phpclass Example {    public $public = 'prop:public'; private $prv   = 'prop:private'; protected $prt = 'prop:protected';}$arrayobj = new ArrayObject(new Example());var_dump($arrayobj->count());$arrayobj = new ArrayObject(array('first','secon 

Результат виконання цього прикладу:

int(1)
int(3)
