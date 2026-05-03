# Agente para Padronização de User Stories

Este repositório contém um prompt para um agente de IA especializado em criar e padronizar User Stories (US) seguindo as melhores práticas de agilidade. O agente atua como um Product Owner Sênior, coletando informações essenciais de forma inteligente e gerando uma User Story completa em formato Markdown.

## Funcionalidades

- **Coleta da Tríade**: O agente solicita as três informações essenciais de uma vez (COMO, QUERO, PARA), validando se cada campo é específico o suficiente antes de gerar.
- **Geração com Qualidade**: Gera uma User Story completa com Descrição, Contexto, Regras de Negócio (RN), Comportamento Esperado (CT), Critérios de Aceitação (CA), Estimativa, Riscos (RIS), Dependências (DEP), Sugestões de Testes e Definição de Pronto (DoD).
- **Siglas Padronizadas**: Todos os itens das seções são prefixados com sigla sequencial e nome descritivo (ex: `RN1 — Nome`, `CA1 — Nome`, `RIS1 — Nome`).
- **Revisão e Iteração**: Apresenta a US gerada, permite ajustes pontuais e só salva após aprovação do usuário.
- **Arquivo de Saída**: Salva a User Story em um arquivo `.md` na pasta `outputs/`, nomeado em formato slug (ex: `filtrar-visualizar-idade-funcionarios-cadastro.md`).

## Como Usar

1. **Configuração**: Certifique-se de que o arquivo `agent.prompt.md` esteja disponível no seu ambiente de IA (ex: VS Code com GitHub Copilot).

2. **Invocação**: Inicie o agente informando a funcionalidade desejada, ou aguarde as perguntas da tríade.

3. **Respostas**: Forneça as três informações de uma vez ou sequencialmente:
   - **COMO**: Papel/ator específico (ex: "Analista de RH").
   - **QUERO**: Ação específica (ex: "filtrar funcionários por idade").
   - **PARA**: Valor de negócio (ex: "identificar quais estão próximos de se aposentar").

4. **Revisão**: O agente apresenta a US gerada e pergunta se há ajustes antes de salvar.

5. **Aprovação**: Confirme ou solicite alterações. Ao aprovar, o arquivo é salvo em `outputs/`.

## Exemplo de Uso

**Usuário:**
> COMO Analista de RH, QUERO filtrar funcionários por idade, PARA identificar quais estão próximos de se aposentar.

**Agente:** Gera a User Story completa com RNs, CTs, CAs, estimativa, riscos e dependências, e pergunta se há ajustes.

**Usuário:** Salvar.

**Agente:** User Story salva em `outputs/filtrar-visualizar-idade-funcionarios-cadastro.md`.

## Estrutura do Arquivo Gerado

```markdown
# [Título da User Story]

## Descrição
Como [COMO], quero [QUERO] para [PARA].

## Contexto
- Domínio: [domínio]
- Tipo de Usuário: [descrição]
- Objetivo de Negócio: [objetivo]

## Regras de Negócio (RN)
- **RN1 — [Nome da Regra]**: [Descrição específica]

## Comportamento Esperado (CT)
- **CT1 — [Nome do Comportamento]**: [Descrição da interação]

## Critérios de Aceitação (CA)
- **CA1 — [Nome do Cenário]**: Dado [contexto], quando [ação], então [resultado esperado]

## Estimativa
- **Complexidade**: [Baixa/Média/Alta]
- **Pontos Sugeridos**: [fibonacci]
- **Justificativa**: [breve explicação]

## Riscos (RIS)
- **RIS1 — [Nome do Risco]**: [Descrição e mitigação]

## Dependências (DEP)
- **DEP1 — [Nome da Dependência]**: [Descrição]

## Sugestões de Testes
- [Teste automatizado]
- [Teste manual]
- [Edge case]

## Definição de Pronto (DoD)
- Código revisado e aprovado
- Testes unitários com cobertura mínima de 80%
- Testes de integração passando
- Documentação atualizada
- QA aprovado

## Prioridade
[Alta/Média/Baixa] - [Justificativa]

## Notas Adicionais
[Informações extras relevantes]
```

## Pré-requisitos

- Ambiente de IA compatível com prompts customizados (ex: GitHub Copilot no VS Code).
- Pasta `outputs/` criada no diretório do projeto.

## Contribuição

Sinta-se à vontade para sugerir melhorias no prompt ou no README.

## Licença

Este projeto é de uso livre para fins educacionais e profissionais.
