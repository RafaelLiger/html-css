<!-- .github/copilot-instructions.md
   Instruções concisas para agentes AI que editam este repositório
   Gerado automaticamente — por favor revise e peça ajustes. -->

# Resumo do projeto
- Projeto: exercício estático HTML/CSS (Desafio 10).
- Entrada principal: `mainsite.html` (arquivo estático, sem build system).
- Estilos: `style.css` no mesmo diretório do HTML.
- Recursos: fontes e imagens em `Materias/pacote-projeto-d010/`.

# Objetivo do agente
- Fazer alterações locais em HTML/CSS, organizar recursos estáticos e propor melhorias front-end pequenas.
- Não adicionar ferramentas de build, dependências externas ou alterar estrutura de pastas sem instrução explícita do humano.

# Padrões e decisões descobertas
- Arquivo de entrada único: `mainsite.html` — edite este arquivo para alterar markup.
- Arquivo de estilo global: `style.css` — global (não há frameworks ou preprocessadores detectados).
- Recursos (fontes/imagens): mantidos em `Materias/pacote-projeto-d010/` e referenciados por caminhos relativos.
- Não há scripts JS, portanto qualquer comportamento dinâmico deve ser acordado antes de adicionar novos arquivos JS.

# Convenções de edição
- Mantenha paths relativos (ex.: `style.css`, `Materias/pacote-projeto-d010/fontes/idroid.otf`).
- Preserve a codificação UTF-8 e o `@charset "UTF-8"` em `style.css`.
- Evite renomear pastas sob `Materias/` — parecem ser recursos de curso/backup.

# Exemplos concretos
- Adicionar uma folha de estilo adicional:
  - Coloque `novo-estilo.css` no mesmo diretório que `mainsite.html` e adicione `<link rel="stylesheet" href="novo-estilo.css">` no `<head>`.
- Referenciar a fonte incluída:
  - Exemplo de `@font-face` em `style.css`:
    ```css
    @font-face { font-family: 'IDroid'; src: url('Materias/pacote-projeto-d010/fontes/idroid.otf') format('opentype'); }
    body { font-family: 'IDroid', sans-serif; }
    ```

# Restrições detectadas
- Não há package manager / scripts de build — não crie `package.json` ou pipeline sem aprovação.
- Não há testes automatizados detectados — não adicionar frameworks de teste.

# Fluxos e integração
- Fluxo típico de edição: editar `mainsite.html` + `style.css` → abrir no browser local (file://) para validação.
- Recursos estáticos são consumidos por HTML via caminhos relativos.

# O que perguntar ao humano antes de mudanças maiores
- Deseja introduzir JS ou um sistema de build (ex.: Parcel, npm)?
- Podemos reorganizar `Materias/` para `assets/`? (impacta caminhos relativos em HTML/CSS).
- Regras de estilo/nomes de classes (ex.: BEM) — há preferência?

# Checklist rápido para PRs criadas por agentes
- Alterações confinadas a HTML/CSS e recursos estáticos.
- Paths relativos testados abrindo `mainsite.html` localmente.
- `style.css` mantém `@charset "UTF-8"` e sem reformatar arquivo sem razão.

# Onde olhar no repositório
- `mainsite.html` — entrada do site.
- `style.css` — estilos globais.
- `Materias/pacote-projeto-d010/` — fontes e imagens (ex.: `idroid.otf`, `dan-droids.png`).

-- Fim do arquivo
