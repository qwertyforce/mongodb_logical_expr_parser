# mongodb_logical_expression_parser
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
