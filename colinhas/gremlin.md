# Apache TinkerPop/Gremlin

## Usar ids com tipo customizado no gremlin server (tinkergraph-empty.properties)
```
gremlin.tinkergraph.vertexIdManager=ANY
```

## Acessar servidor remoto no gremlin console
```
:remote connect tinkerpop.server conf/remote.yaml session
:remote config timeout none
:remote console
```

### Links úteis:

PRACTICAL GREMLIN - An Apache TinkerPop Tutorial: https://kelvinlawrence.net/book/Gremlin-Graph-Guide.html
sql2gremlin: http://sql2gremlin.com
25+ Handy Gremlin Examples and Code Snippets for Graph Database Traversal and Manipulation: https://www.fromdev.com/2013/09/Gremlin-Example-Query-Snippets-Graph-DB.html
Gremlin standards compliance in Amazon Neptune: https://docs.aws.amazon.com/neptune/latest/userguide/access-graph-gremlin-differences.html