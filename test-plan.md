# 📋 Plano de Testes Manuais - Sistema de Delivery de Comida

---

## 🔹 Funcionalidade 1: Cadastro de novos restaurantes

| Funcionalidade           | Cenário de Teste                                | Passos                                                                                                                                      | Resultado Esperado                                                                 |
|--------------------------|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Cadastro de restaurante  | Cadastro com dados válidos                      | 1. Acessar o painel de administração<br>2. Selecionar "Cadastro de restaurantes"<br>3. Preencher todos os campos obrigatórios<br>4. Clicar em "Salvar" | Mensagem:Restaurante cadastrado com sucesso. Usuário é redirecionado para a lista de restaurantes.           |
| Cadastro de restaurante  | CNPJ inválido                                   | Preencher o campo CNPJ com um valor inválido (ex: "123456789") e clicar em "Salvar"                                                        | Mensagem de erro: "CNPJ inválido". Cadastro não é concluído.                      |
| Cadastro de restaurante  | CNPJ duplicado                                  | Cadastrar um restaurante com um CNPJ já existente no sistema                                                                                | Mensagem de erro: "CNPJ já cadastrado". Cadastro não é concluído.                 |
| Cadastro de restaurante  | Campo obrigatório ausente                       | Omitir o preenchimento de campos obrigatórios como nome, telefone ou endereço                                                              | Mensagem de erro informando os campos obrigatórios não preenchidos.              |


---

## 🔹 Funcionalidade 2: Cadastro de cardápios

| Funcionalidade         | Cenário de Teste                                | Passos                                                                                                                                             | Resultado Esperado                                                                 |
|------------------------|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Cadastro de cardápio   | Cadastro com dados válidos                      | 1. Acessar o painel de administração<br>2. Selecionar "Cadastro de cardápios"<br>3. Selecionar um restaurante<br>4. Preencher nome e descrição<br>5. Adicionar itens com nome, descrição e preço válidos<br>6. Clicar em "Salvar" | Cardápio cadastrado com sucesso e redirecionamento para lista de cardápios.       |
| Cadastro de cardápio   | Nome do cardápio ausente                        | Deixar o campo "nome do cardápio" em branco e tentar salvar                                                                                       | Mensagem de erro: "Nome do cardápio é obrigatório".                               |
| Cadastro de cardápio   | Nome de item ausente                            | Adicionar um item ao cardápio sem preencher o nome                                                                                                 | Mensagem de erro: "Nome do item é obrigatório".                                   |
| Cadastro de cardápio   | Preço inválido                                  | Inserir um valor não numérico ou negativo no campo preço                                                                                           | Mensagem de erro: "Preço inválido".                                               |
| Cadastro de cardápio   | Nome duplicado de cardápio no mesmo restaurante | Tentar cadastrar dois cardápios com o mesmo nome para o mesmo restaurante                                                                         | Mensagem de erro: "Já existe um cardápio com esse nome para este restaurante".    |


---

