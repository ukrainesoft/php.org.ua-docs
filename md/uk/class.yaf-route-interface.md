- [« Yaf_Response_Abstract::\_\_toString](yaf-response-abstract.tostring.md)
- [Yaf_Route_Interface::assemble »](yaf-route-interface.assemble.md)

- [PHP Manual](index.md)
- [Yaf](book.yaf.md)
- Клас Yaf_Route_Interface

# Клас Yaf_Route_Interface

(Yaf \>=1.0.0)

## Вступ

**Yaf_Route_Interface** використовується для завдання власного
маршрутизації.

## Огляд класів

class **Yaf_Route_Interface** {

/\* Методи \*/

abstract public [assemble](yaf-route-interface.assemble.md)(array
`$info`, array `$query` = ?): string

abstract public
[route](yaf-route-interface.route.md)([Yaf_Request_Abstract](class.yaf-request-abstract.md)
`$request`): bool

}

## Зміст

- [Yaf_Route_Interface::assemble](yaf-route-interface.assemble.md) -
Збирає запит
- [Yaf_Route_Interface::route](yaf-route-interface.route.md) -
Надсилання запиту
