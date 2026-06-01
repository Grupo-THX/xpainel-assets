![Logo do XPainel](https://xpainel.com/site/images/main-logo.png)
# xPainel Rental Code Icons

Repositorio de assets CSS e fontes de icones usados no xPainel.

## Uso rapido

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Grupo-THX/xpainel-assets/icons.css">
```

## Padrao de organizacao de pastas

Sempre manter cada biblioteca no formato abaixo:

```text
fonts/{biblioteca}/{versao}/css/
fonts/{biblioteca}/{versao}/fonts/
```

Exemplo real (Remix Icon):

```text
fonts/remixicon/4.9.1/css/remixicon.css
fonts/remixicon/4.9.1/fonts/remixicon.woff2
fonts/remixicon/4.9.1/fonts/remixicon.woff
```

Regra importante:
- Nao criar pasta de biblioteca na raiz do repositorio.
- CSS sempre em css/ e arquivos de fonte sempre em fonts/.
- Preferir caminho relativo no CSS da propria biblioteca, apontando para ../fonts/.

## Como adicionar uma nova fonte de icones

1. Criar estrutura de pastas com nome da biblioteca e versao.
2. Copiar CSS da biblioteca para a pasta css/.
3. Copiar arquivos de fonte para a pasta fonts/.
4. Ajustar urls no CSS da biblioteca para caminhos locais (sem depender de CDN externo).
5. Adicionar import no arquivo icons.css.
6. Commit e push no GitHub.
7. Fazer purge no jsDelivr.

## Exemplo de import no icons.css

```css
@import url('fonts/remixicon/4.9.1/css/remixicon.css');
```

## Purge no jsDelivr (obrigatorio apos push)

Ferramenta:
- https://www.jsdelivr.com/tools/purge

URLs recomendadas para purge:

```text
https://cdn.jsdelivr.net/gh/Grupo-THX/xpainel-assets
https://cdn.jsdelivr.net/gh/Grupo-THX/xpainel-assets/icons.css
```

E tambem as URLs da biblioteca adicionada. Exemplo Remix:

```text
https://cdn.jsdelivr.net/gh/Grupo-THX/xpainel-assets/fonts/remixicon/4.9.1/css/remixicon.css
https://cdn.jsdelivr.net/gh/Grupo-THX/xpainel-assets/fonts/remixicon/4.9.1/fonts/remixicon.woff2
https://cdn.jsdelivr.net/gh/Grupo-THX/xpainel-assets/fonts/remixicon/4.9.1/fonts/remixicon.woff
```

Observacao:
- Se aparecer Throttled no purge, aguarde alguns segundos e tente novamente a mesma URL.

## Checklist final

- Estrutura de pastas padronizada
- Import adicionado em icons.css
- CSS da biblioteca apontando para arquivos locais
- Push realizado
- Purge executado
