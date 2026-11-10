# Desenho Curricular de Inteligência Artificial

Ferramenta web para montar propostas de grade curricular de IA, organizando unidades, descrições e cargas horárias em uma interface visual.

## Objetivo

Apoiar o planejamento curricular com uma biblioteca inicial de 13 unidades sobre fundamentos de IA, dados, prompts, automação, infraestrutura, aprendizado de máquina, ética e projeto integrador.

## Funcionalidades

- Arrastar unidades entre a biblioteca e a grade.
- Criar e editar nome, descrição e carga horária.
- Reordenar unidades e calcular a carga horária total.
- Remover unidades e desfazer exclusões.
- Importar unidades de arquivos JSON ou TXT com conteúdo JSON.
- Exportar a proposta da grade em PDF.

## Como usar

1. Clone ou baixe o repositório, mantendo `index.html` e `logo.png` na mesma pasta.
2. Abra `index.html` no navegador e clique em **Iniciar**.
3. Arraste as unidades desejadas para **Grade Curricular**.
4. Edite as unidades e confira a carga horária.
5. Use **Exportar PDF** para guardar a proposta.

A aplicação mantém as alterações em memória durante a sessão. Ao recarregar a página, a biblioteca inicial é reconstruída.

## Formato de importação

O arquivo deve conter uma lista JSON com `name`, `hours` e, opcionalmente, `desc`:

```json
[
  {
    "name": "Fundamentos de Inteligência Artificial",
    "hours": 16,
    "desc": "Conceitos, aplicações e limitações da IA."
  }
]
```

As unidades importadas são adicionadas à grade existente.

## Tecnologias e estrutura

- HTML, CSS e JavaScript.
- API de arrastar e soltar do navegador.
- jsPDF 2.5.1 para gerar PDF.
- Font Awesome e Google Fonts para ícones e tipografia.

| Arquivo | Finalidade |
| --- | --- |
| `index.html` | Interface, estilos e lógica da aplicação |
| `logo.png` | Identidade visual |

As dependências externas são carregadas por CDN e precisam de internet. A ferramenta organiza conteúdo curricular; não executa modelos de IA.
