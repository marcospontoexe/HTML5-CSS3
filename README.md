# HTML5 & CSS3

Repositório de estudos de **HTML5** e **CSS3**: material didático organizado por tópico, exercícios e **projetos completos** desenvolvidos ao longo de três cursos.

🌐 **Todos os projetos estão publicados e podem ser abertos no navegador:** <https://marcospontoexe.github.io/HTML5-CSS3/>

---

## Índice

- [Projetos desenvolvidos](#projetos-desenvolvidos)
- [Apostilas](#apostilas)
- [Cursos de origem](#cursos-de-origem)
- [Estrutura do repositório](#estrutura-do-repositório)
- [Como executar localmente](#como-executar-localmente)

---

## Projetos desenvolvidos

### Sites completos (CSS puro)

| Projeto | Descrição | Técnicas | Código | Demo |
|---|---|---|---|---|
| **Museu Nacional** | Site institucional de página única, com galeria, seções de história e contato. | Flexbox, float, layout de seções | [04-museu](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/04-museu) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/04-museu/index.html) |
| **Chalé Hotel** | Site de hotelaria com **9 páginas** navegáveis: home, história, gastronomia, reserva, imprensa, contato e 3 páginas regionais (PR, SC, RS). | Layout multipágina, float, navegação | [03-Site_Chale](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/03-Site_Chale) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/03-Site_Chale/home.html) |
| **Notícias Cidade** | Portal de notícias com **7 editorias** (Brasil, Internacional, Economia, Ciências, Saúde, Fotos). | Layout em colunas, float, grid editorial | [02-site_noticias](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/02-site_noticias) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/02-site_noticias/home.html) |
| **Blog** | Layout de blog com barra lateral e listagem de posts. | Box model, posicionamento | [01-blog](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/01-blog) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/01-blog/index.html) |
| **Café Fontenebleu** | Site de restaurante com **7 páginas**: home, info, eventos, DVD, localização, menu e avaliações. | Variáveis CSS, `@font-face`, float, layout com sidebar | [01-Restaurante](HTML/Material%20did%C3%A1tico/Udemy/Desenvolvedor%20web%20completo/PROJETOS/01-Restaurante) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/HTML/Material%20did%C3%A1tico/Udemy/Desenvolvedor%20web%20completo/PROJETOS/01-Restaurante/home.html) |

### Projetos com Bootstrap 4

| Projeto | Descrição | Técnicas | Código | Demo |
|---|---|---|---|---|
| **Spotify (landing page)** | Página promocional "Música para todos", responsiva. | Bootstrap 4, media queries, float | [03-spotify](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/BOOTSTRAP-4/PROJETOS/03-spotify) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/BOOTSTRAP-4/PROJETOS/03-spotify/index.html) |
| **Finans** | Landing page de app de finanças pessoais. | Bootstrap 4, grid, componentes | [02-finans](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/BOOTSTRAP-4/PROJETOS/02-finans) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/BOOTSTRAP-4/PROJETOS/02-finans/index.html) |
| **Projeto padrão** | Estrutura base (boilerplate) para iniciar projetos Bootstrap. | Bootstrap 4, grid | [01-projeto-padrao](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/BOOTSTRAP-4/PROJETOS/01-projeto-padrao) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/BOOTSTRAP-4/PROJETOS/01-projeto-padrao/index.html) |

### Desafios do Curso em Vídeo

| Projeto | Descrição | Técnicas | Código | Demo |
|---|---|---|---|---|
| **Como surgiu o mascote do Android** | Artigo com tipografia customizada, favicon e navegação semântica. | `@font-face`, HTML semântico, tipografia | [01-android](CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/01-android) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/01-android/android.html) |
| **Cordel Moderno** | Página com imagens de fundo e estilização de texto poético. | `background-image`, tipografia | [03-cordel](CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/03-cordel) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/03-cordel/index.html) |
| **Astronauta** | Composição de imagens sobrepostas com fundo espacial. | Posicionamento, camadas | [02-astronauta](CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/02-astronauta) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/02-astronauta/index.html) |
| **Rede social (iframes)** | Página que carrega Facebook, Instagram, GitHub e YouTube em `<iframe>`. | `<iframe>`, navegação interna | [13-iframe](HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/Desafios/13-iframe) | [Abrir](https://marcospontoexe.github.io/HTML5-CSS3/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/Desafios/13-iframe/index.html) |

---

## Apostilas

Anotações de estudo escritas ao longo dos cursos, com exemplos comentados:

- 📘 **[Apostila de HTML](HTML/README.md)** — estrutura do documento, headings, imagens, links, listas, tabelas, semântica e formulários.
- 🎨 **[Apostila de CSS](CSS/README.md)** — regras e seletores, box model, `padding`/`margin`, variáveis, tipografia, tabelas, formulários e layout flexível.

Cada seção das apostilas aponta para a pasta de exemplos correspondente.

---

## Cursos de origem

| # | Curso | Plataforma | Material neste repositório |
|---|---|---|---|
| 1 | **Curso de HTML5 e CSS3 — Módulos 1 a 5** ([M1](https://www.youtube.com/playlist?list=PLHz_AreHm4dkZ9-atkcmcBaMZdmLHft8n), [M2](https://www.youtube.com/playlist?list=PLHz_AreHm4dlUpEXkY1AyVLQGcpSgVF8s), [M3](https://www.youtube.com/playlist?list=PLHz_AreHm4dmcAviDwiGgHbeEJToxbOpZ), [M4](https://www.youtube.com/playlist?list=PLHz_AreHm4dkcVCk2Bn_fdVQ81Fkrh6WT), [M5](https://www.youtube.com/playlist?list=PLHz_AreHm4dn1bAtIJWFrugl5z2Ej_52d)) | Curso em Vídeo (YouTube) | [HTML/Curso em vídeo](HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo) · [CSS/Curso_em_Vídeo](CSS/material_didatico/Curso_em_V%C3%ADdeo) |
| 2 | **[Desenvolvedor Web Completo](https://www.udemy.com/course/curso-desenvolvedor-web-completo/)** | Udemy | [HTML/Udemy](HTML/Material%20did%C3%A1tico/Udemy/Desenvolvedor%20web%20completo) · [CSS/Udemy](CSS/material_didatico/Udemy/Desenvolvedor%20web%20completo) |
| 3 | **[Desenvolvimento Web Completo](https://www.udemy.com/course/web-completo/)** | Udemy | [CSS/Desenvolvimento Web Completo 2022](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022) |

---

## Estrutura do repositório

```
HTML5-CSS3/
├── HTML/
│   ├── README.md                 ← apostila de HTML
│   └── Material didático/
│       ├── Curso em vídeo/       ← 1-sintaxe … 11-formulario + Desafios
│       └── Udemy/                ← formulários + PROJETOS
└── CSS/
    ├── README.md                 ← apostila de CSS
    └── material_didatico/
        ├── Curso_em_Vídeo/       ← 01-estilos … 10-mediaquery + desafios
        └── Udemy/                ← seletores, box, flexbox, BOOTSTRAP-4, PROJETOS
```

**Tópicos cobertos**

- **HTML** — sintaxe, imagens, emoji, títulos, semântica, listas, links, mídias (áudio/vídeo), tabelas, iframe, formulários.
- **CSS** — estilos (inline/interno/externo), cores, tipografia, alinhamento, seletores, caixas, variáveis, responsividade, imagens de fundo, media queries, posicionamento, overflow, colunas, box-sizing, animação, flexbox.
- **Bootstrap 4** — 20 tópicos, de formatação de texto a grid, flexbox e carousel.

Cada pasta de lição é **autocontida**: traz seu próprio HTML, CSS, imagens e fontes, e pode ser aberta isoladamente.

---

## Como executar localmente

Os projetos são estáticos — basta abrir o arquivo `.html` no navegador:

```powershell
Start-Process "CSS\material_didatico\Curso_em_Vídeo\desafios\01-android\android.html"
```

Para projetos que usam fontes locais ou recursos que o protocolo `file://` bloqueia, sirva a pasta por HTTP:

```powershell
python -m http.server 8000
# depois acesse http://localhost:8000
```

---

## Licença

Distribuído sob a licença [MIT](LICENSE). O material didático pertence aos respectivos autores dos cursos.
