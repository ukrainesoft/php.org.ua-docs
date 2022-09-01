---
navigation:
  - commonmark-cql.construct.html: '« CommonMarkCQL::construct'
  - ref.cmark.html: Функции CommonMark »
  - index.html: PHP Manual
  - class.commonmark-cql.html: CommonMarkCQL
title: 'CommonMarkCQL::invoke'
---
# CommonMarkCQL::invoke

(cmark >= 1.1.0)

CommonMarkCQL::invoke — Виконання CQL

### Опис

```methodsynopsis
public CommonMark\CQL::__invoke(CommonMark\Node $root, callable $handler)
```

Повинен викликати поточну функцію CQL у зазначеному `root`, виконуючи вказаний `handler` при вході в [CommonMarkNode](class.commonmark-node.html)

### Список параметрів

`root`

кореневий вузол дерева

`handler`

повинен мати прототип:

```methodsynopsis
handler(CommonMark\Node $root, CommonMark\Node $entering): ?bool
```

-   Якщо `handler` нічого не повертає (void) або повертає null, CQL продовжить виконання
-   Якщо обробник поверне справжнє значення, CQL продовжить виконання
-   Якщо обробник повертає хибне значення, CQL припинить виконання
