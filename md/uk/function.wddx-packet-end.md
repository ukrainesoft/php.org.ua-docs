Завершує пакет WDDX із зазначеним ідентифікатором

-   [« wddxdeserialize](function.wddx-deserialize.html)
    
-   [wddxpacketstart »](function.wddx-packet-start.html)
    
-   [PHP Manual](index.html)
    
-   [Функції WDDX](ref.wddx.html)
    
-   Завершує пакет WDDX із зазначеним ідентифікатором
    

# wddxpacketend

(PHP 4, PHP 5, PHP 7)

wddxpacketend — Завершує пакет WDDX із зазначеним ідентифікатором

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_packet_end(resource $packet_id): string
```

Завершує та повертає заданий пакет WDDX.

### Список параметрів

`packet_id`

Пакет WDDX, що повертається [wddxpacketstart()](function.wddx-packet-start.html)

### Значення, що повертаються

Повертає рядок, який містить пакет WDDX.