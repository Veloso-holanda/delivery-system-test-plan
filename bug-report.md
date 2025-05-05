
# 🐞 Relatório de Bug - Cadastro de Entregadores

## 📌 Descrição do bug
Ao cadastrar um novo entregador, o sistema **aceita qualquer sequência de números no campo CPF**, mesmo que seja um CPF inválido ou com formatação incorreta. Após preencher os dados e clicar em "Enviar", o sistema **conclui o cadastro sem apresentar mensagens de erro**, violando as regras de negócio.

---

## ✅ Passos para reproduzir o bug

1. Acesse a página de **cadastro de entregadores**.
2. Preencha todos os campos obrigatórios com dados válidos, **exceto o CPF** (informe um número inválido, como `12345678900`).
3. Clique no botão **"Enviar"**.
4. Observe que o sistema **finaliza o cadastro com sucesso**, sem validar o CPF.

---

## 🚨 Prioridade do bug
**Alta** – O erro permite o cadastro de entregadores sem CPF válido, o que pode gerar problemas legais, fiscais e comprometer a integridade dos dados da base.

---

## ⚠️ Possíveis impactos no sistema

- Cadastro de entregadores com documentos inválidos ou inexistentes.
- Problemas com a **emissão de notas fiscais** e integração com sistemas contábeis.
- Fragilidade na **segurança e confiabilidade** do sistema.
- Risco de **fraude** ou uso indevido da plataforma por usuários sem identificação válida.

---

# 📣 Ações após criação do card no JIRA

## 1. Notificar o desenvolvedor responsável (Back-end)
Como a validação do CPF é uma responsabilidade de back-end:

- Entrar em contato direto com **Bruno**, o desenvolvedor back-end.
- Compartilhar o link do card no JIRA com ele e explicar verbalmente o problema e a gravidade.

> Exemplo de mensagem:  
> “Oi Bruno, tudo bem? Encontrei um bug importante no cadastro de entregadores: o sistema está aceitando CPFs inválidos. Criei o card no JIRA com todos os detalhes e evidências. Pode dar uma olhada o quanto antes? Qualquer coisa estou aqui para ajudar nos testes depois da correção!”

## 2. Comunicar a gerente de projeto (Carol)
- Informar a **Carol** sobre o bug e seus impactos na confiabilidade e possíveis riscos legais.
- Enviar o link do card e explicar por que isso deve ser tratado como prioridade.

> Exemplo de mensagem:  
> “Oi Carol, passando pra te avisar de um bug crítico que encontrei no cadastro de entregadores. O sistema está aceitando qualquer CPF, mesmo inválido, o que pode gerar problemas sérios com notas fiscais e credibilidade. Criei o card no JIRA com todos os detalhes. Recomendo que reavaliemos as prioridades do sprint.”

## 3. Acompanhar a correção
- Estar disponível para **testar novamente** a funcionalidade assim que Bruno aplicar a correção.
- Repetir os testes com CPFs válidos e inválidos para confirmar que a validação está funcionando.
- Atualizar o card no JIRA para **"Em teste"** e depois **"Concluído"**, após a verificação.

## 4. Prevenção futura
- Sugerir à equipe uma **revisão geral das validações nos formulários**.
- Reforçar a importância de **testes exploratórios manuais**, mesmo em funcionalidades aparentemente simples.
