Проводить перевірку tcpwrap

-   [« Функції TCP](ref.tcpwrap.html)
    
-   [Varnish »](book.varnish.html)
    
-   [PHP Manual](index.html)
    
-   [Функції TCP](ref.tcpwrap.html)
    
-   Проводить перевірку tcpwrap
    

# tcpwrapcheck

(PECL tcpwrap >= 0.1.0)

tcpwrapcheck — Проводить перевірку tcpwrap

### Опис

```methodsynopsis
tcpwrap_check(    string $daemon,    string $address,    string $user = ?,    bool $nodns = false): bool
```

Функція звіряється з файлами /etc/hosts.allow та /etc/hosts.deny для перевірки, чи можна чи не можна дати доступ клієнту до демона `daemon`

### Список параметрів

`daemon`

Ім'я Сервісу.

`address`

Адреса клієнта. Може бути як доменним ім'ям, так і IP-адресою.

`user`

Необов'язкове ім'я користувача.

`nodns`

Якщо адреса `address` виглядає як доменне ім'я, то робиться запит до DNS для визначення його IP-адреси. Для блокування такої поведінки встановіть `nodns` на значення **`true`**

### Значення, що повертаються

Повертає **`true`**, якщо доступ дозволено та **`false`**, якщо ні.

### Приклади

**Приклад #1 Заборона всіх з'єднань з локального хоста**

Якщо у /etc/hosts.deny є запис:

php: 127.0.0.1

І ваш код виглядає якось так:

```php
<?php
if (!tcpwrap_check('php', $_SERVER['REMOTE_ADDR'])) {
  die('Вас тут не ждут');
}
?>
```

### Дивіться також

Для отримання більш детальної інформації зверніться до документації по hostsaccess(3).