---
navigation:
  - parle-parser.dump.md: '« ParleParser::dump'
  - parle-parser.left.md: 'ParleParser::left »'
  - index.md: PHP Manual
  - class.parle-parser.md: ParleParser
title: 'ParleParser::errorInfo'
---
# ParleParser::errorInfo

(PECL parle >= 0.5.1)

ParleParser::errorInfo — Отримує інформацію про помилку

### Опис

```methodsynopsis
public Parle\Parser::errorInfo(): Parle\ErrorInfo
```

Отримує інформацію про помилку у разі, якщо **ParleParser::action()** повернув дію у разі виникнення помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр [ParleErrorInfo](class.parle-errorinfo.md)
