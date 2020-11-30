# Testes automatizados com ruby e rspec

## Comandos

Criar arquivo de dependências de projeto ruby
```
bundle init
```

Instalar dependências
```
bundle install
```

Criar arquivo de configuração do rspec
```
rspec --init
```

Formatar como documento (visualização dos testes fica mais legível)
```
rspec -fd
```

Executar linha específica
```
rspec -fd spec/teste_spec.rb:6
```

Agrupar testes por tag
```
it "Testando soma", :soma do
   expect(calculadora.soma(1, 2)).to eq(3)
end

```
```
rspec -t soma
```

## Interpolando variáveis em string:
"Olá #{nome_da_variavel}" válido\
'Olá #{nome_da_variavel}' inválido\
É necessário usar aspas duplas para interpolar strings

## Possíveis erros

### "Process failed: spawn rdebug-ide.bat ENOENT"
Executar:
```
gem install ruby-debug-ide
```
Vide: https://github.com/rubyide/vscode-ruby/issues/113

### Links úteis:

Iniciando testes de serviços com HTTParty e RSpec: https://medium.com/cwi-software/https-medium-com-maximilianoalves-iniciando-testes-de-servicos-com-httparty-e-rspec-366fe93525ab
