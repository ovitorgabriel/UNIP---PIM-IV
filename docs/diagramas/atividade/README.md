# Diagramas de Atividade – Aprender Mais

## O que é um diagrama de atividade?

O diagrama de atividade é um diagrama comportamental da UML que mostra o **fluxo de trabalho** de um processo: a sequência de ações executadas, as **decisões** (caminhos "sim/não") e os pontos em que o fluxo começa e termina. Funciona como um fluxograma padronizado pela UML.

Cada diagrama de casos de uso já tem seu diagrama de sequência. A diferença entre os dois é:

| Diagrama | Pergunta que responde | Foco |
|---|---|---|
| Casos de uso | **O que** o sistema faz e **quem** usa? | Funcionalidades e atores |
| Sequência | **Quais objetos trocam mensagens** e em que ordem? | Comunicação entre objetos/classes |
| **Atividade** | **Como o processo flui** e o que acontece em cada decisão? | Fluxo, regras e caminhos alternativos |

Por isso, cada diagrama de atividade aqui inclui os **fluxos alternativos**: dados inválidos, usuário não encontrado, cancelamento etc.

## Notação utilizada

| Símbolo | Significado |
|---|---|
| ● (círculo preenchido) | Nó inicial: onde a atividade começa |
| Retângulo arredondado | Ação: um passo executado |
| ◇ (losango) com `[sim]` / `[não]` | Nó de decisão: o fluxo segue por um caminho conforme a condição |
| ◇ sem texto | Nó de junção (*merge*): caminhos alternativos voltam a se unir |
| ◉ (círculo com borda) | Nó final da atividade: o processo terminou |
| ⊗ (círculo com X) | Final de fluxo: aquele caminho termina, sem concluir o objetivo |
| Colunas (raias / *swimlanes*) | Quem executa cada ação: **ator** (Aluno, Secretaria, ADM ou Usuário), **Sistema** e **Banco de Dados** |

## Diagramas

| Caso de uso | Ator | Imagem | Fonte |
|---|---|---|---|
| UC01 – Acessar sistema | Usuário | [png](png/UC01-acessar-sistema.png) | [puml](src/UC01-acessar-sistema.puml) |
| UC02 – Realizar cadastro | Usuário | [png](png/UC02-realizar-cadastro.png) | [puml](src/UC02-realizar-cadastro.puml) |
| UC03 – Acessar conteúdos/avaliações | Aluno | [png](png/UC03-acessar-conteudos.png) | [puml](src/UC03-acessar-conteudos.puml) |
| UC04 – Realizar avaliações | Aluno | [png](png/UC04-realizar-avaliacoes.png) | [puml](src/UC04-realizar-avaliacoes.puml) |
| UC05 – Acessar notas | Aluno | [png](png/UC05-acessar-notas.png) | [puml](src/UC05-acessar-notas.puml) |
| UC06 – Avaliar atividades | Secretaria | [png](png/UC06-avaliar-atividades.png) | [puml](src/UC06-avaliar-atividades.puml) |
| UC07 – Adicionar conteúdos | Secretaria | [png](png/UC07-adicionar-conteudos.png) | [puml](src/UC07-adicionar-conteudos.puml) |
| UC08 – Editar conteúdos | Secretaria | [png](png/UC08-editar-conteudos.png) | [puml](src/UC08-editar-conteudos.puml) |
| UC09 – Desativar conteúdos | Secretaria | [png](png/UC09-desativar-conteudos.png) | [puml](src/UC09-desativar-conteudos.puml) |
| UC10 – Cadastrar secretaria | ADM | [png](png/UC10-cadastrar-secretaria.png) | [puml](src/UC10-cadastrar-secretaria.puml) |
| UC11 – Desativar cadastros | ADM | [png](png/UC11-desativar-cadastros.png) | [puml](src/UC11-desativar-cadastros.puml) |

Os fluxos seguem as descrições e os diagramas de sequência de cada caso de uso no arquivo do Astah (`../casos-de-uso/Diagrama de casos de uso.asta`).

## Como editar e regerar

Os diagramas são escritos em **PlantUML**: texto que vira imagem.

- **Online:** cole o conteúdo do `.puml` em <https://www.plantuml.com/plantuml> (copie também o bloco do `_estilo.puml` ou remova a linha `!include`).
- **VS Code:** instale a extensão *PlantUML* e pressione `Alt+D` para pré-visualizar.
- **Linha de comando** (requer Java):

```bash
cd docs/diagramas/atividade/src
java -jar plantuml.jar -charset UTF-8 -tpng -o ../png UC*.puml
```

Se o professor exigir os diagramas dentro do Astah, use as imagens em `png/` como referência e redesenhe em **Astah → Diagram → Activity Diagram**, adicionando as *partitions* (raias) Ator / Sistema / Banco de Dados.
