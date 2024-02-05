---
navigation:
  - commonmark-cql.construct.md: '« CommonMark\\CQL::\_\_construct'
  - ref.cmark.md: Функції CommonMark »
  - index.md: PHP Manual
  - class.commonmark-cql.md: CommonMark\\CQL
title: 'CommonMark\\CQL::\_\_invoke'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CommonMark\\CQL::\_\_invoke

(cmark >= 1.1.0)

CommonMark\\CQL::\_\_invoke — Виконання CQL

### Опис

```methodsynopsis
public CommonMark\CQL::__invoke(CommonMark\Node $root, callable $handler)
```

Повинен викликати поточну функцію CQL у зазначеному `root`, виконуючи вказаний `handler`при входе в[CommonMark\\Node](class.commonmark-node.md)

### Список параметрів

`root`

кореневий вузол дерева

`handler`

повинен мати прототип:

```methodsynopsis
handler(CommonMark\Node $root, CommonMark\Node $entering): ?bool
```

-   Якщо `handler`нічого не повертає (void) або повертає null, CQL продовжить виконання
-   Якщо обробник поверне справжнє значення, CQL продовжить виконання
-   Якщо обробник повертає хибне значення, CQL припинить виконання
