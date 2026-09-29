# CONTEXTO DA SESSÃO

- **Última atualização:** 2026-09-29 06:32
- **Sessão nº:** 2
- **Status geral:** em andamento

## 1. Objetivo da tarefa
Transformar este repositório de estudos numa vitrine de portfólio: completar os projetos, deixar o [README.md](README.md) fiel ao conteúdo real e praticar um fluxo de branch/PR que recrutadores possam ver no GitHub.

## 2. Já feito ✅
- [CLAUDE.md](CLAUDE.md): guia do repositório + regra de handoff adaptada.
- [README.md](README.md): vitrine com demos ao vivo; as descrições foram auditadas contra o conteúdo real.
- Café Fontenebleu (7 páginas), Museu Nacional (7 páginas) e Chalé Hotel (5 páginas com conteúdo) estão na `main`. O PR do Chalé foi fundido (`20e783d`).
- [_config.yml](_config.yml) com `exclude:`: verificado em 2026-09-29, `/CLAUDE.html` e `/rascunho.html` respondem 404 no site.
- Notícias Cidade: `internacional`, `economia`, `saude` e `ciencias` escritas com o layout de 3 colunas da home; README e doc de detalhes atualizados (**não commitado**).
- Estado e restrições de cada projeto: [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md).

## 3. Em andamento 🔧
- O trabalho do Notícias Cidade está **não commitado, com a `main` aberta na IDE**. Arquivos: os 4 HTML em [02-site_noticias](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/02-site_noticias), [README.md](README.md), [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md) e este arquivo.
- Próximo passo imediato: **criar a branch `feat/noticias-editorias` antes de commitar** (as alterações vão junto para ela), commitar e abrir o PR.

## 4. Próximos passos (planejado) 📋
1. Branch, commits e PR do Notícias Cidade.
2. Decidir sobre os erros de digitação originais do Notícias ("Nova legistação" na home, "Renato ROdrigues" na lateral das 6 páginas) e o rodapé em `<p>` de `brasil` e `fotos` (texto preto sobre azul).
3. Notícias: completar `brasil.html` e `fotos.html`.
4. Chalé: criar `reserva.html`, `rg.html`, `sc.html` e `pr.html`.
5. Blog e Projeto padrão: desenvolver ou deixar fora da vitrine.
6. Montar o portfólio usando as URLs do Pages.

## 5. Decisões e raciocínio 🧠
- O Pages publica a partir de `main` / (root), então **a `main` é o site no ar**: trabalho grande passa por branch + PR.
- O README só afirma o que foi verificado pela contagem de palavras visíveis.
- Os detalhes ficam em [.claude/docs/](.claude/docs/), não em `DOCS/`: o Jekyll ignora pastas que começam com ponto.
- Conteúdo fictício: nenhum ID de YouTube inventado, nenhum veículo de imprensa real, pessoas com nomes fictícios.
- Notícias: a lateral é copiada igual à da home (com os erros de digitação, por consistência); nenhum link novo para `#`.
- PRs em inglês. Squash quando os commits da branch tiverem mensagens ruins.

## 6. Estado do projeto / ambiente
- Branch atual: `main` = `origin/main` = `9b5a61c` (último commit: `Update rascunho.md`, feito direto na `main`).
- Arquivos não commitados: ver seção 3.
- `git` **fora do PATH**: commits e PRs são feitos pela IDE e pelo GitHub web; o estado do git é lido direto em `.git`.
- Python 3.14 disponível; node/npx não.
- Site: <https://marcospontoexe.github.io/HTML5-CSS3/>.

## 7. Bloqueios e pendências ⚠️
- O projeto 13-iframe expõe links do Facebook e do Instagram pessoais na vitrine. A decisão é do usuário.
- Corrigir ou não os erros de digitação originais do Notícias (ver seção 4, item 2).

## 8. Comandos úteis
- Servir um projeto localmente (embeds do YouTube falham em `file://`):
  `python -m http.server 8000 --directory "<pasta do projeto>"`
- Ver o estado do git sem o `git`: `Get-Content .git\HEAD`, a pasta `.git\refs\heads\` e o arquivo `.git\logs\HEAD`.
- Comparar um arquivo entre branches ou commits: `https://raw.githubusercontent.com/marcospontoexe/HTML5-CSS3/<branch-ou-sha>/<caminho>`.
- **Atenção:** trocar de branch na IDE troca os arquivos do disco. Confira `.git\HEAD` antes de concluir que algo "sumiu".

## 9. Como retomar
Leia este arquivo e [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md), confirme a branch atual em `.git\HEAD` e continue a partir da seção 3 (branch e PR do Notícias Cidade).
