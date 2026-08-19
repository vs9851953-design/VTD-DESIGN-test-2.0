# VTD Design — Portfolio

Portfolio estático em HTML, CSS e JavaScript puro. Não usa React, npm, GSAP, Lenis ou outras dependências de runtime.

## Estrutura

- `index.html` — página inicial
- `project.html?id=...` — página de cada projeto
- `portfolio.json` — único arquivo para cadastrar projetos
- `css/` — estilos
- `js/` — carregamento e animações
- `projects/<id>/` — `cover.jpg` + imagens `gallery-1.jpg`, `gallery-2.jpg` etc.

## Adicionar projeto

No `portfolio.json`, cadastre:

```json
{
  "id": "meu-projeto",
  "titulo": "Meu Projeto",
  "categoria": "Design",
  "ano": "2026",
  "cliente": "Cliente",
  "descricao": "Descrição do projeto.",
  "feedback": "Depoimento.",
  "feedbackAutor": "Nome",
  "feedbackCargo": "Cargo",
  "cover": "projects/meu-projeto/cover.jpg",
  "gallery": [
    "projects/meu-projeto/gallery-1.jpg",
    "projects/meu-projeto/gallery-2.jpg"
  ]
}
```

Não é obrigatório ter `thumb`. Na página inicial, o sistema usa `thumb` se existir e, caso contrário, usa `cover`.

## Vercel

É um site estático. Basta importar o repositório no Vercel. Não é necessário configurar build command ou instalar dependências.
