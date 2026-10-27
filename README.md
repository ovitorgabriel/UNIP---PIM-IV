# PIM IV – Aprender Mais

Projeto Integrado Multidisciplinar IV – Curso Superior de Tecnologia em Análise e Desenvolvimento de Sistemas (UNIP).

**Tema:** Desenvolvimento e implantação de uma solução tecnológica corporativa integrada para apoiar a transformação digital de uma empresa. É a continuação do [PIM III](https://github.com/souzaa7/PIM_III), onde foram feitos o levantamento de requisitos e a modelagem.

**Aprender Mais** é uma plataforma educacional responsiva (web e mobile) voltada ao ensino de Tecnologia da Informação, com três perfis de acesso: **Aluno**, **Secretaria** e **ADM**.

## Estrutura

```text
docs/
└── diagramas/
    ├── casos-de-uso/
    │   └── Diagrama de casos de uso.asta   # casos de uso + diagramas de classes e sequência (Astah)
    └── atividade/
        ├── README.md                       # o que é um diagrama de atividade + índice
        ├── src/                            # fontes PlantUML (.puml)
        ├── png/                            # imagens para o documento do PIM
        └── svg/                            # imagens vetoriais
```

## Casos de uso

| ID | Caso de uso | Ator |
|---|---|---|
| UC01 | Acessar sistema | Usuário |
| UC02 | Realizar cadastro | Usuário |
| UC03 | Acessar conteúdos/avaliações | Aluno |
| UC04 | Realizar avaliações | Aluno |
| UC05 | Acessar notas | Aluno |
| UC06 | Avaliar atividades | Secretaria |
| UC07 | Adicionar conteúdos | Secretaria |
| UC08 | Editar conteúdos | Secretaria |
| UC09 | Desativar conteúdos | Secretaria |
| UC10 | Cadastrar secretaria | ADM |
| UC11 | Desativar cadastros | ADM |

Diagramas de atividade de cada caso de uso: [docs/diagramas/atividade](docs/diagramas/atividade/README.md).
