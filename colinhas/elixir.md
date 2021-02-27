# Elixir/Phoenix

## Instalar phoenix
```
mix archive.install hex phx_new 1.57
```

## Criar novo projeto
```
mix phx.new my-project
```

## Criar novo projeto sem depedências web
```
mix phx.new rocketpay --no-webpack --no-html
```

## Checar se database está configurada
```
mix ecto.setup
```

## Instalar pacotes
```
mix deps.get
```

## Criar arquivo de configuração do credo
```
mix credo gen.config
```

## Iniciar servidor
```
mix phx.server
```

## Compilador interativo
```
iex
```

## Compilador interativo vinculado ao projeto atual
```
iex -S mix
```

## Recompilar projeto
```
iex  
recompile
```

## Ver help de módulo qualquer
```
h String
```

## Executar testes
```
mix test
```