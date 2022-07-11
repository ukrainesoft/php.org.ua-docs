- [«Yar_Server](class.yar-server.md)
- [Yar_Server::handle »](yar-server.handle.md)

- [PHP Manual](index.md)
- [Yar_Server](class.yar-server.md)
- Конструктор Yar_Server

# Yar_Server::\_\_construct

(PECL yar \> = 1.0.0)

Yar_Server::\_\_construct - Конструктор Yar_Server

### Опис

final public **Yar_Server::\_\_construct**(Object `$obj`)

Встановлює сервер Yar HTTP RPC. Усі публічні методи об'єкта $obj
буде зареєстровано як RPC-сервіси.

### Список параметрів

`obj`
Об'єкт, публічні методи якого будуть зареєстровані як
RPC-Сервіси.

### Значення, що повертаються

Об'єкт класу [Yar_Server](class.yar-server.md).

### Приклади

**Приклад #1 Приклад використання **Yar_Server::\_\_construct()****

` <?phpclass API {    /**    * the doc info will be generated automatically into service info page. * @params     * @return     */    public function some_method($parameter, $option = "foo") {          me }   protected function client_can_not_see() {    }}$service = new Yar_Server(new API());$service->handle();?> `

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

- [Yar_Server::handle()](yar-server.handle.md) - Запустити сервер
RPC
