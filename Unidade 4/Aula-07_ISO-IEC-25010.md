# ═══════ Estudo de Caso: Sistema Acadêmico ═══════

> **Integrante:** Sara Rebeca do Rosario Soares
**Grupo:** 3 a 5 estudantes (foi feita apenas por uma pessoa) | **Tempo:** 20 min | **Valor:** 0,5 ponto


## Visão geral

| # | Problema | Característica | 
|---|----------|----------------|
| 1 | Média com valores incorretos | Adequação funcional |
| 2 | Página de notas demora 12 s | Desempenho |
| 3 | Difícil achar a renovação de matrícula | Usabilidade |
| 4 | App cai com muitos usuários | Confiabilidade |
| 5 | Estudante viu histórico de outro | Segurança |
| 6 | Alteração no cadastro quebra outros módulos | Manutenibilidade |
| 7 | Não importa dados do financeiro | Compatibilidade |
| 8 | Novo servidor exige ajustes manuais | Portabilidade |
| 9 | Equipamento acionado sob condição insegura | Segurança funcional (safety) |

## Análise por problema 𓆉 ⋆.˚𓇼 ⋆.˚𓆟

### 1. Média com valores incorretos °‧🫧⋆.ೃ࿔*:･

| Item | Resposta |
|------|----------|
| Característica | Adequação funcional (correção) |
| Justificativa | O resultado calculado está errado. |
| Requisito | O sistema deve calcular a média conforme a fórmula oficial da instituição. |
| Critério de aceitação | 100% das médias de teste conferem com o resultado esperado. |
| Como testar | Teste funcional comparando com planilha de referência. |

### 2. Página de notas demora 12 s 🪼⋆.ೃ࿔*:･

| Item | Resposta |
|------|----------|
| Característica | Eficiência de desempenho |
| Justificativa | O resultado está correto, mas o tempo de resposta é alto. |
| Requisito | A página de notas deve abrir em até 3 segundos. |
| Critério de aceitação | 95% das requisições respondem em até 3 s. |
| Como testar | Teste de carga (ex.: JMeter). |

### 3. Difícil achar a renovação de matrícula ⭒₊ ⊹🌕₊ ⊹⭒

| Item | Resposta |
|------|----------|
| Característica | Usabilidade |
| Justificativa | A função existe, mas o usuário não a encontra. |
| Requisito | A renovação de matrícula deve estar a no máximo 2 cliques da tela inicial. |
| Critério de aceitação | 90% dos usuários encontram a função em até 30 s, sem ajuda. |
| Como testar | Teste de usabilidade com tarefa cronometrada. |

### 4. App cai com muitos usuários ˙✧˖°📷 ༘ ⋆｡˚

| Item | Resposta |
|------|----------|
| Característica | Confiabilidade |
| Justificativa | O sistema para de funcionar sob carga. |
| Requisito | O sistema deve suportar o número de usuários simultâneos definido sem cair. |
| Critério de aceitação | Sem quedas durante todo o teste com a carga-alvo. |
| Como testar | Teste de carga e estresse. |

### 5. Estudante viu histórico de outro ˚ ༘ 🦕𖦹⋆｡˚

| Item | Resposta |
|------|----------|
| Característica | Segurança (confidencialidade) |
| Justificativa | Dados de um usuário foram expostos a outro. |
| Requisito | Cada estudante deve acessar somente os seus próprios dados. |
| Critério de aceitação | Nenhum acesso a dados de terceiros, mesmo alterando URL ou parâmetros. |
| Como testar | Teste de controle de acesso manipulando IDs e URLs. |

### 6. Alteração no cadastro quebra outros módulos ⋆.ೃ࿔🌸*:･

| Item | Resposta |
|------|----------|
| Característica | Manutenibilidade (modularidade) |
| Justificativa | Uma mudança local afetou módulos não relacionados (alto acoplamento). |
| Requisito | Alterações no cadastro não devem afetar os demais módulos. |
| Critério de aceitação | 100% dos testes de regressão dos outros módulos passam após a alteração. |
| Como testar | Testes de regressão automatizados. |

### 7. Não importa dados do financeiro ִֶָ. ..𓂃 ࣪ ִֶָ🪽་༘࿐

| Item | Resposta |
|------|----------|
| Característica | Compatibilidade (interoperabilidade) |
| Justificativa | O sistema não troca dados corretamente com outro sistema. |
| Requisito | O sistema deve importar dados do financeiro no formato definido (CSV ou API). |
| Critério de aceitação | Arquivo de teste importado sem erros, com 100% dos registros corretos. |
| Como testar | Teste de integração com dados de exemplo. |

### 8. Novo servidor exige ajustes manuais ﹒⌗﹒🦇﹒౨ৎ˚₊‧

| Item | Resposta |
|------|----------|
| Característica | Portabilidade (instalabilidade) |
| Justificativa | O sistema não se adapta bem a um novo ambiente. |
| Requisito | O sistema deve ser instalável em novo servidor com configuração mínima e automatizada. |
| Critério de aceitação | Instalação concluída em até X passos, sem alterar código-fonte. |
| Como testar | Teste de implantação em servidor limpo ou container. |

### 9. Equipamento acionado sob condição insegura ☆⋆｡𖦹°‧★

| Item | Resposta |
|------|----------|
| Característica | Segurança funcional (safety) |
| Justificativa | Há risco físico a pessoas e equipamentos. |
| Requisito | O sistema não deve acionar o equipamento se as condições de segurança não forem atendidas. |
| Critério de aceitação | Acionamento bloqueado em 100% dos testes com condição insegura. |
| Como testar | Teste funcional simulando condições inseguras. |
