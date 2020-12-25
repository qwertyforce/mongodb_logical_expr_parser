# mongodb_logical_expression_parser
```javascript
build_ast("a&&(b||c)")
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
