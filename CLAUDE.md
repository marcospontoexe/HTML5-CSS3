# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## O que é este repositório

Repositório **pessoal de estudos** de HTML5 e CSS3, em **português (pt-BR)**. Não é uma aplicação: não há build system, gerenciador de pacotes, linter nem testes. O conteúdo é composto por:

1. **Dois documentos-apostila** — são o "produto" principal do repositório:
   - [HTML/README.md](HTML/README.md) (~26 KB) — sintaxe, headings, imagens, links, listas, tabelas, semântica, formulários.
   - [CSS/README.md](CSS/README.md) (~44 KB) — regra CSS, tipos de CSS, seletores, box model, `padding`/`margin`, variáveis, texto, tabelas, formulários.
2. **Exemplos executáveis** em [HTML/Material didático/](HTML/Material%20didático/) e [CSS/material_didatico/](CSS/material_didatico/), organizados por curso de origem (Curso em Vídeo, Udemy, Origamid) e numerados por tópico (`01-estilos`, `02-cores`, …, `10-mediaquery`), mais pastas `desafios`/`Desafios` e `PROJETOS`.

Os READMEs **linkam para as pastas de exemplo** correspondentes. Ao adicionar um exemplo novo, adicione também o link no README do tópico — esse é o índice de navegação do repositório.

## Executar e pré-visualizar

Não há comando de build. As páginas são estáticas e abrem direto no navegador:

```powershell
Start-Process "CSS\material_didatico\Curso_em_Vídeo\desafios\01-android\android.html"
```

Para casos que exigem servidor HTTP (fontes locais, `file://` bloqueado, media queries com recursos externos):

```powershell
python -m http.server 8000    # python 3.14 disponível; node/npx NÃO estão instalados
```

Não existe "rodar um teste": a verificação é visual, abrindo a página e redimensionando a janela / usando o DevTools.

## Restrições do ambiente (importantes)

- **`git` não está no PATH** desta máquina. Comandos `git ...` pelo PowerShell falham com `CommandNotFoundException`. Use as operações de git da IDE/interface, ou peça ao usuário. Não tente descobrir histórico via shell.
- **Caminhos com acentos, espaços e parênteses** são a norma (`Material didático`, `Curso_em_Vídeo`, `03-tipografia(fontes)`, `05-semântica (formatação)`). Sempre coloque os caminhos entre aspas duplas no PowerShell.
- Nos links de Markdown, esses caracteres precisam ser **URL-encoded** (`Curso_em_V%C3%ADdeo`, `%20` para espaço) — é o padrão já usado nos READMEs.

## Convenções

- **Idioma:** todo o conteúdo, comentários de código e nomes de pasta são em português. `<html lang="pt-br">` e `<meta charset="UTF-8">` em todos os documentos.
- **Estrutura típica de uma pasta de lição:** um `.html` de entrada + subpastas `style/` ou `estilo/` ou `css/`, `imagens/` (ou `imgens/` na raiz de CSS — a grafia está assim, não "corrija"), `fontes/`. O arquivo de entrada nem sempre se chama `index.html`; muitas lições usam o nome do tópico (`variaveis.html`, `formulario.html`, `android.html`).
- **Cada pasta de lição é autocontida.** Bibliotecas de terceiros são vendorizadas por lição — existem **20 cópias** de `bootstrap.min.css` (uma por lição de `BOOTSTRAP-4/`), além de Font Awesome e Open Iconic com seus `.less`/`.scss`/`.styl`/`.map`. Isso é intencional (cada lição abre isolada). **Não** consolide em uma pasta compartilhada e **não** edite arquivos dentro de `fontawesome/`, `iconic/` ou `bootstrap*`.
- **Imagens dos READMEs:** as figuras são referenciadas com URLs `https://github.com/marcospontoexe/HTML5-CSS3/blob/main/...`, que o GitHub **não renderiza como imagem** (blob devolve uma página HTML). Ao adicionar figuras novas, prefira caminho relativo (`imgens/1.jpeg`) ou `raw.githubusercontent.com`. Ao mexer nas existentes, avise o usuário antes de trocar o padrão em massa.

## GitHub Pages

Há duas configurações Jekyll: [_config.yml](_config.yml) na raiz (`jekyll-theme-minimal`) e [docs/_config.yml](docs/_config.yml) (`jekyll-theme-cayman`). O conteúdo de [docs/index.md](docs/index.md) ainda é o **template padrão do GitHub Pages**, não conteúdo do projeto.

> ⚠️ **Não escreva em [docs/](docs/)** para notas de trabalho. Essa pasta é publicada como site. Ver a adaptação de `DOCS/` na regra de handoff abaixo.

## Artefatos pré-existentes que não devem ser "limpos"

Já estão commitados e não há `.gitignore` na raiz: `HTML/Material didático/Curso em vídeo/2-imagens/.vs/` (estado do Visual Studio), vários `.DS_Store`, `meulivro.zip`, `HandBrake-1.4.2-x86_64-Win_GUI.exe` e `destino.php` (alvo de exemplo de formulário, sem backend). Não remova nem adicione `.gitignore` sem pedir ao usuário.

---

# Regra: Persistência de Contexto (Handoff entre sessões)

## Objetivo

Garantir que nenhum trabalho se perca quando a sessão atual se tornar demasiado longa. O agente deve gravar todo o estado da sessão num ficheiro de handoff, de forma que **qualquer outro chat consiga retomar exatamente de onde parou**, com o mesmo contexto.

---

## Gatilho

Execute o procedimento de salvamento abaixo **antes de continuar qualquer tarefa** sempre que uma das seguintes condições for atingida:
1. A conversa prolongar-se por muitas interações (aproximando-se do limite prático da janela de contexto).
2. Uma funcionalidade ou milestone importante for concluída.
3. O utilizador disser explicitamente: `salvar contexto`, `handoff` ou `checkpoint`.

---

## Procedimento de salvamento

1. **Termine** a tarefa atual.
2. Crie ou atualize o arquivo **[CONTEXTO.md](CONTEXTO.md)** na raiz do projeto.
   - Se já existir, **atualize** as seções em vez de duplicar (mantenha o histórico relevante, remova o que já foi superado).
   - Sempre atualize o campo de data/hora e o número da sessão.
3. Preencha **todas** as seções do template abaixo. Não deixe seções vazias — escreva "nenhum" quando não houver conteúdo.
4. Confirme ao usuário que o contexto foi salvo e informe o caminho do arquivo.
5. **Gestão do CONTEXTO.md:** Mantenha este arquivo enxuto. Adicione a ele apenas um **índice** que aponte para ficheiros com o contexto detalhado de cada tópico. O objetivo é não sobrecarregar a janela de contexto ao ler o [CONTEXTO.md](CONTEXTO.md) no diretório raiz; caso precise de mais informações sobre um tópico, aceda ao ficheiro específico.

   > **Adaptação obrigatória neste projeto:** a regra original manda guardar os detalhes em `DOCS/`. Aqui isso **não funciona** — o Windows não diferencia maiúsculas de minúsculas, então `DOCS/` é a mesma pasta que [docs/](docs/), que é publicada pelo GitHub Pages. Neste repositório, grave os ficheiros detalhados em **[.claude/docs/](.claude/docs/)** (ignorada pelo Jekyll, não vai para o site).

---

## Template do `CONTEXTO.md`

```markdown
# CONTEXTO DA SESSÃO

- **Última atualização:** AAAA-MM-DD HH:MM
- **Sessão nº:** N
- **Status geral:** (em andamento | bloqueado | pronto para revisão)

## 1. Objetivo da tarefa
Descrição em 1–3 frases do que estamos tentando alcançar (o "porquê").

## 2. Já feito ✅
- Itens concluídos, com o(s) arquivo(s) afetado(s).
- Ex.: "Implementado endpoint POST /login em `src/auth.py`"

## 3. Em andamento 🔧
- O que estava sendo feito no momento do checkpoint.
- Em qual arquivo/linha parei e qual era o próximo passo imediato.

## 4. Próximos passos (planejado) 📋
- Lista ordenada do que falta fazer.
- Quanto mais específico, melhor (arquivo, função, comportamento esperado).

## 5. Decisões e raciocínio 🧠
- Escolhas técnicas feitas e o porquê.
- Alternativas descartadas (para evitar refazer a análise).
- Suposições assumidas.

## 6. Estado do projeto / ambiente
- Arquivos-chave e o papel de cada um.
- Branch git atual, alterações não commitadas, migrations pendentes, etc.
- Variáveis de ambiente ou dependências relevantes.

## 7. Bloqueios e pendências ⚠️
- Erros não resolvidos, dúvidas para o usuário, decisões aguardando aprovação.

## 8. Comandos úteis
- Comandos para rodar/testar/buildar o projeto.
- Ex.: `npm run dev`, `pytest tests/`, etc.

## 9. Como retomar
Instrução direta para o próximo chat: "Leia este arquivo e continue a partir
da seção 3 / passo X."
```

---

## Como retomar em um novo chat

No início de qualquer nova sessão, o agente deve:

1. Verificar se existe o ficheiro [CONTEXTO.md](CONTEXTO.md) na raiz do projeto.
2. Se existir, **lê-lo por completo antes de qualquer outra ação**.
3. Resumir ao utilizador em 2–3 linhas onde o trabalho parou e qual é o próximo passo, e então continuar.

> Comando sugerido para o utilizador iniciar um novo chat:
> **"Leia o `CONTEXTO.md` e continue de onde a sessão anterior parou."**

---

## Boas práticas

- **Escreva para um estranho:** o próximo chat não tem memória nenhuma; seja explícito.
- **Caminhos absolutos ou relativos à raiz**, nunca referências vagas ("aquele arquivo").
- **Não salve segredos** (tokens, senhas, chaves) no `CLAUDE.md` nem no `CONTEXTO.md`.
- **Um arquivo por projeto:** mantenha o `CONTEXTO.md` enxuto; arquive versões antigas em `CONTEXTO.arquivo.md` se necessário.
- **Commit opcional:** se o usuário usar git, ofereça commitar o `CONTEXTO.md` para que ele persista entre máquinas. (Neste repo, lembre-se: `git` não está no PATH — ver "Restrições do ambiente" acima.)
- **Feedback de alterações:** Caso algum ficheiro seja alterado durante a sessão, informe sempre qual o ficheiro e o que foi alterado no final de cada mensagem.
- **Referenciar diretórios e arquivos através de links:** Sempre que se referir a um diretório ou arquivo local, use link e não backticks.
