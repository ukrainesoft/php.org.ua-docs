Експортувати сокет у потік, що інкапсулює сокет

-   [« socketcreate](function.socket-create.html)
    
-   [socketgetoption »](function.socket-get-option.html)
    
-   [PHP Manual](index.md)
    
-   [Функции сокета](ref.sockets.md)
    
-   Експортувати сокет у потік, що інкапсулює сокет
    

# socketexportstream

(PHP 7> = 7.0.7, PHP 8)

socketexportstream — Експортувати сокет у потік, що інкапсулює сокет

### Опис

```methodsynopsis
socket_export_stream(Socket $socket): resource|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`socket`

### Значення, що повертаються

Повертає ресурс або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |