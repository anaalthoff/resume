## Protocolo de Despacho e Handoff de Agentes

### Tabela de Roteamento
- **A – Scout**: Busca de vagas.
- **B – Curator**: Busca de cursos.
- **C – Coach**: Simulação de entrevista.
- **D – Maestro**: Lida com o quiz e orquestra o fluxo.

### Envelope de Despacho (usado pelo Maestro)
```
## DESPACHO: [NOME_DO_AGENTE]
### referencia_persona
[Conteúdo completo de personas/<nome_do_agente_minusculo>.md]

### tarefa
[Uma frase descrevendo o que o agente deve fazer]

### perfil_usuario
[Conteúdo de data/user-profile.md]

### contexto
[Contexto específico: ex: qual vaga para entrevistar, quais habilidades buscar cursos]

### saida_esperada
[Formato exato que o agente deve retornar]
```

### Envelope de Resposta (retornado pelos agentes despachados)
```
## RESPOSTA: [NOME_DO_AGENTE]
### estado
[sucesso | erro]

### resumo
[Resumo legível de 2‑3 frases para o usuário]

### dados
[Resultados como listas numeradas com pares chave‑valor. Sem tabelas markdown.]

### erros
[Apenas se estado for erro: o que deu errado]
```

### Especificações de Handoff por Agente
- **Scout**: Recebe `contexto` com filtros de vaga; devolve lista de vagas.
- **Curator**: Recebe `contexto` com lacunas de habilidades; devolve lista de cursos.
- **Coach**: Recebe `contexto` com vaga alvo; realiza 6 despachos sequenciais (perguntas de entrevista) e devolve avaliação.
- **Maestro**: Gerencia o quiz, gera `user-profile.md` e apresenta o menu.

### Despacho Sequencial do Coach (6 etapas)
1. Pergunta de introdução.
2. Pergunta de experiência técnica.
3. Pergunta de soft‑skills.
4. Pergunta de situação‑comportamento.
5. Pergunta de desafio técnico.
6. Feedback final.

### Regras de Tratamento de Erros
- Se um agente retornar `estado: erro`, o Maestro deve incluir o campo `erros` no envelope de resposta ao usuário.
- Caso falha de ferramenta (ex.: `spawn_agent` não iniciar), registrar o erro em `erros` e oferecer opção de retry.
- Não prosseguir silenciosamente após erro; sempre comunicar ao usuário.
