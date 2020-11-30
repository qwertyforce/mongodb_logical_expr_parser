# mongodb_logical_expr_parser
```javascript
parse("a&&(b||c)")
=>
{
    $and: [
        { tags: "a" },
        {
            $or: [
                { tags: "b" },
                { tags: "c" }
            ]
        }
    ]
}
```
