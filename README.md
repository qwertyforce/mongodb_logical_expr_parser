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
```javascript
build_ast("forest&&height>=1920&&width>=1080")
=>
{
   "$and":[
      {
         "$and":[
            {"tags":"forest"},
            {"height":{"$gte":1920}}
         ]
      },
      {"width":{"$gte":1080}}
   ]
}
```
