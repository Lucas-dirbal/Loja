# Como usar Git neste projeto

Este projeto esta em um repositorio Git. Use este guia para salvar suas alteracoes, enviar para o repositorio remoto e manter sua copia atualizada.

## Entrar na pasta do projeto

```sh
cd "/home/lucas/Área de trabalho/Loja"
```

## Ver o estado do projeto

Antes de salvar ou enviar qualquer coisa, veja o que mudou:

```sh
git status
```

Versao curta:

```sh
git status --short
```

## Ver detalhes das alteracoes

Para ver exatamente o que foi alterado nos arquivos:

```sh
git diff
```

## Adicionar arquivos para o commit

Adicionar todos os arquivos modificados:

```sh
git add .
```

Adicionar apenas um arquivo especifico:

```sh
git add index.html
git add script.js
git add stylr.css
```

## Criar um commit

Depois de adicionar os arquivos, salve um ponto na historia do projeto:

```sh
git commit -m "Descreve aqui o que foi alterado"
```

Exemplos:

```sh
git commit -m "Atualiza layout da loja"
git commit -m "Corrige script do carrinho"
git commit -m "Ajusta estilos da pagina inicial"
```

## Enviar para o repositorio remoto

Depois do commit, envie para o remoto:

```sh
git push
```

Se for o primeiro push de uma branch nova:

```sh
git push -u origin nome-da-branch
```

## Atualizar seu projeto com o remoto

Antes de comecar a trabalhar, e uma boa pratica buscar as ultimas alteracoes:

```sh
git pull
```

## Fluxo recomendado do dia a dia

```sh
git pull
git status
git add .
git commit -m "Mensagem curta explicando a mudanca"
git push
```

## Criar uma branch para testar mudancas

Criar e entrar em uma branch nova:

```sh
git checkout -b minha-mudanca
```

Ver branches existentes:

```sh
git branch
```

Voltar para a branch principal:

```sh
git checkout main
```

## Desfazer alteracoes com cuidado

Desfazer alteracoes de um arquivo que ainda nao foi commitado:

```sh
git restore nome-do-arquivo
```

Exemplo:

```sh
git restore index.html
```

Se o arquivo ja foi adicionado com `git add`, tire ele da area de commit:

```sh
git restore --staged nome-do-arquivo
```

## Mensagens de commit boas

Prefira mensagens curtas e claras:

```text
Adiciona menu de navegacao
Corrige responsividade do layout
Atualiza estilos dos produtos
Remove codigo nao usado
```

Evite mensagens vagas:

```text
mudancas
teste
arrumei coisa
```

## Comandos mais usados

```sh
git status
git diff
git add .
git commit -m "Mensagem do commit"
git push
git pull
```

## Observacao importante

Evite usar comandos destrutivos, como `git reset --hard`, sem ter certeza do que esta fazendo. Eles podem apagar alteracoes locais.
