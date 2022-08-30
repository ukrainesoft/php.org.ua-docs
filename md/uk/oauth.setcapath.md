Встановити CA для шляху та інформації

-   [« OAuth::setAuthType](oauth.setauthtype.html)
    
-   [OAuth::setNonce »](oauth.setnonce.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Встановити CA для шляху та інформації
    

# OAuth::setCAPath

(PECL OAuth >= 0.99.8)

OAuth::setCAPath — Встановити CA для шляху та інформації

### Опис

```methodsynopsis
public OAuth::setCAPath(string $ca_path = ?, string $ca_info = ?): mixed
```

Встановити центр сертифікації (CA) для шляхів та інформації.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`ca_path`

CA шляху.

`ca_info`

CA інформації.

### Значення, що повертаються

Повертає **`true`** або \*\*`false`\*\*якщо будь-який з параметрів `ca_path` або `ca_info` заданий некоректно.

### список змін

| Версия           | Описание                                                                   |
|------------------|----------------------------------------------------------------------------|
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |

### Дивіться також

-   [OAuth::getCaPath()](oauth.getcapath.html) - Отримати інформацію CA