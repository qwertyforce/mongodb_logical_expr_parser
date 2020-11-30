# mongodb_logical_expr_parser
```
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
