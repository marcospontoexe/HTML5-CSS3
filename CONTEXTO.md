# CONTEXTO DA SESSÃO

- **Última atualização:** 2026-09-29 21:53
- **Sessão nº:** 2
- **Status geral:** em andamento

## 1. Objetivo da tarefa
Transformar este repositório de estudos numa vitrine de portfólio: completar os projetos, deixar o [README.md](README.md) fiel ao conteúdo real e praticar um fluxo de branch/PR que recrutadores possam ver no GitHub.

## 2. Já feito ✅
- [CLAUDE.md](CLAUDE.md): guia do repositório + regra de handoff adaptada.
- [README.md](README.md): vitrine com demos ao vivo; as descrições foram auditadas contra o conteúdo real.
- Na `main`: Café Fontenebleu (7 páginas), Museu Nacional (7), Chalé Hotel (5 com conteúdo), Notícias Cidade (home + 4 editorias) e Curiosidades de Tecnologia, o projeto 01-android (4 páginas, com os erros antigos do artigo corrigidos; PR fundido em `28ff80a`).
- [_config.yml](_config.yml) com `exclude:`: `/CLAUDE.html` e `/rascunho.html` respondem 404 no site.
- Formulários de contato do Museu e do Chalé corrigidos: passaram de `post` (erro 405 no GitHub Pages) para `get` + confirmação via `:target` (commitado, ainda não enviado).
- Formulário "Agende uma visita", na lateral das 7 páginas do Museu: ganhou confirmação via `:target` (`action="#agendado"`) e data obrigatória (**não commitado**).
- Estado e restrições de cada projeto: [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md).

## 3. Em andamento 🔧
- Branch `fix/broken-form-submission` (criada da `main` em `28ff80a`), com 2 commits locais **ainda não enviados**: `fix: submit contact forms with GET...` e `docs: update handoff notes`.
- Arquivos não commitados: as 7 páginas HTML e o `CSS/style.css` do [Museu](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/04-museu) (formulário de visita), [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md) e este arquivo.
- Próximo passo imediato: commitar o formulário de visita, enviar a branch e abrir o PR.

## 4. Próximos passos (planejado) 📋
1. Commit, envio e PR dos formulários (contato do Museu e do Chalé + agendamento de visita do Museu).
2. Notícias: corrigir "Renato ROdrigues" nas 6 páginas; completar `brasil.html` e `fotos.html` (o rodapé em `<p>` fica preto sobre azul).
3. Chalé: criar `reserva.html`, `rg.html`, `sc.html` e `pr.html`.
4. Blog e Projeto padrão: desenvolver ou deixar fora da vitrine.
5. Montar o portfólio usando as URLs do Pages.

## 5. Decisões e raciocínio 🧠
- O Pages publica a partir de `main` / (root), então **a `main` é o site no ar**: trabalho grande passa por branch + PR.
- O README só afirma o que foi verificado pela contagem de palavras visíveis.
- Os detalhes ficam em [.claude/docs/](.claude/docs/), não em `DOCS/`: o Jekyll ignora pastas que começam com ponto.
- Conteúdo fictício nos sites de empresas inventadas. Nas páginas sobre tecnologia real (Android), só fatos verificáveis.
- Formulários usam `get`: o GitHub Pages responde 405 a `post`. Os formulários de lições de curso que usam `post` ficam como estão, porque são o assunto da aula.
- PRs em inglês. Squash só quando os commits da branch tiverem mensagens ruins; com commits bem separados, Rebase and merge.

## 6. Estado do projeto / ambiente
- Branch atual: `fix/broken-form-submission`, local em `7e3a194` (2 commits à frente da `main`, não enviados). `main` = `origin/main` = `28ff80a`.
- Arquivos não commitados: ver seção 3.
- `git` **fora do PATH**: commits e PRs são feitos pela IDE e pelo GitHub web; o estado do git é lido direto em `.git`.
- Python 3.14 disponível; node/npx não.
- Site: <https://marcospontoexe.github.io/HTML5-CSS3/>.

## 7. Bloqueios e pendências ⚠️
- O projeto 13-iframe expõe links do Facebook e do Instagram pessoais na vitrine. A decisão é do usuário.
- Os itens 2 a 4 da seção 4 aguardam o usuário decidir quando fazer (o antigo item opcional do formulário de visita foi feito).

## 8. Comandos úteis
- Servir um projeto localmente (embeds do YouTube falham em `file://`):
  `python -m http.server 8000 --directory "<pasta do projeto>"`
- Ver o estado do git sem o `git`: `Get-Content .git\HEAD`, a pasta `.git\refs\heads\` e o arquivo `.git\logs\HEAD`.
- Comparar um arquivo entre branches ou commits: `https://raw.githubusercontent.com/marcospontoexe/HTML5-CSS3/<branch-ou-sha>/<caminho>`.
- Testar se uma página aceita `POST`: `Invoke-WebRequest -Uri "<url>" -Method Post -Body @{a='b'}` (o GitHub Pages responde 405).
- **Atenção:** trocar de branch na IDE troca os arquivos do disco. Confira `.git\HEAD` antes de concluir que algo "sumiu".

## 9. Como retomar
Leia este arquivo e [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md), confirme a branch atual em `.git\HEAD` e continue a partir da seção 3 (commits e PR da correção dos formulários).
