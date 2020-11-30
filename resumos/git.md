# Git

## Obter última(s) tag(s)
git tag --sort=-v:refname | grep "^[0-9]" -m 20

## Criar tag
git tag 1.10.1

## Ver tag origem
git describe

## Publicar tag
git push -u  origin 1.10.1

## Deletar commit local
git reset --soft HEAD~1

## Deletar branch no servidor
git push origin --delete minha-branch