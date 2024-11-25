# Plano de Testes

## 1. Identificação

- **Projeto**: UI TESTING - e-commerce Sauce Demo 
- **Responsável pelo Plano de Testes**: Matheus Gama
- **Data de Criação**: 23/11/2024
- **Revisão**: 1.0

## 2. Objetivo

Garantir que todas as funcionalidades principais do Swag Labs sejam testadas nos fluxos principais. O foco é garantir que a aplicação seja uma experiência eficiente e acessível para os usuários, cobrindo os seguintes fluxos:

- Fluxo de login.
- Ordenação e filtragem de produtos.
- Processo de compra completo.
- Remoção de itens do carrinho.
- Navegação entre páginas.
- Fluxo de Logout.
- Testes de acessibilidade.

## 3. Escopo dos Testes

### Funcionalidades a serem testadas
- Fluxo de login.
- Ordenação e filtragem de produtos.
- Processo de compra completo.
- Remoção de itens do carrinho.
- Navegação entre páginas.
- Fluxo de Logout.
- Critérios e funcionalidades de acessibilidade.

### Funcionalidades não incluídas no teste
- Testes de automação.
- Testes não funcionais, com exceção dos relacionados à acessibilidade.

## 4. Abordagem

Os testes serão realizados com base nas especificações funcionais e na descrição  técnica do Teste Prático QA Testing BeTalent, utilizando os seguintes tipos de testes:

- **Teste Funcional**: Para validar se as funcionalidades atendem aos requisitos especificados.
- **Teste de Integração**: Para verificar se os módulos funcionam corretamente em conjunto.
- **Teste de Navegação**: Para validar a transição entre páginas e fluxos principais.
- **Teste de Acessibilidade**: Para assegurar que a aplicação está em conformidade, garantindo uma experiência inclusiva para todos os usuários.

## 5. Critérios de Entrada e Saída

### Critérios de Entrada
- Ambiente de teste configurado e validado no Windows 11 e Google Chrome.
- Documentação dos requisitos.
- Credenciais para acessar o e-commerce Sauce Demo.
- Conjunto inicial de dados necessários para a execução de cenário.

### Critérios de Saída
- Execução de todos os casos de teste planejados.
- Identificação e registro de todos os defeitos encontrados.

## 6. Casos de Teste

### **Fluxo de Login**

### **CT001 - Login com usuário “standard_user”**

- **Descrição**: Testar login com credenciais do usuário “standard_user”.
- **Pré-condições**: Usuário registrado com credenciais válidas.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Inserir o nome de usuário “standard_user” e senha “secret_sauce”.
    3. Clique no botão “Login”.
- **Resultado esperado**: O usuário é redirecionado para a página inicial “**Products”**.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT002 - Login com usuário “locked_out_user”**

- **Descrição**: Testar login com credenciais do usuário “locked_out_user”.
- **Pré-condições**: Usuário registrado com credenciais válidas.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Inserir o nome de usuário “locked_out_user” e senha “secret_sauce”.
    3. Clique  no botão “Login”.
- **Resultado esperado**: O usuário é redirecionado para a página inicial “**Products”**.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Reprovado.

### **CT003 - Login com usuário “problem_user”**

- **Descrição**: Testar login com credenciais do usuário “problem_user”.
- **Pré-condições**: Usuário registrado com credenciais válidas.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Inserir o nome de usuário “problem_user” e senha “secret_sauce”.
    3. Clique  no botão “Login”.
- **Resultado esperado**: O usuário é redirecionado para a página inicial “**Products”**.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT004 - Login com usuário “performance_glitch_user”**

- **Descrição**: Testar login com credenciais do usuário “performance_glitch_user”.
- **Pré-condições**: Usuário registrado com credenciais válidas.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Inserir o nome de usuário “performance_glitch_user” e senha “secret_sauce”.
    3. Clique  no botão “Login”.
- **Resultado esperado**: O usuário é redirecionado para a página inicial “**Products”**.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT005 - Login com usuário “error_user”**

- **Descrição**: Testar login com credenciais do usuário “error_user”.
- **Pré-condições**: Usuário registrado com credenciais válidas.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Inserir o nome de usuário “error_user” e senha “secret_sauce”.
    3. Clique  no botão “Login”.
- **Resultado esperado**: O usuário é redirecionado para a página inicial “**Products”**.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT006 - Login com usuário “visual_user”**

- **Descrição**: Testar login com credenciais do usuário “visual_user”.
- **Pré-condições**: Usuário registrado com credenciais válidas.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Inserir o nome de usuário “visual_user” e senha “secret_sauce”.
    3. Clique  no botão “Login”.
- **Resultado esperado**: O usuário é redirecionado para a página inicial “**Products”**.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT007 - Login com credenciais inválidas**

- **Descrição**: Testar login com credenciais inválidas.
- **Pré-condições**: Nenhuma.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Inserir nome de usuário e senha inválidos.
    3. Clique no botão “Login”.
- **Resultado esperado**: Mensagem de erro exibida impossibilitado o login.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT008 - Campo de usuário vazio**

- **Descrição**: Testar login com o campo de usuário vazio.
- **Pré-condições**: Nenhuma.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Deixar o campo “Usuário” vazio e preencher o campo “Senha”.
    3. Clique no botão “Login”.
- **Resultado esperado**: Mensagem de erro exibida: “Username is required”.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT009 - Campo de senha vazio**

- **Descrição**: Testar login com o campo de senha vazio.
- **Pré-condições**: Nenhuma.
- **Passos para execução**:
    1. Acessar a página de login.
    2. Preencher o campo “Usuário” e deixar o campo “Senha” vazio.
    3. Clique no botão “Login”.
- **Resultado esperado**: Mensagem de erro exibida: “Password is required”.
- **Suíte de teste**: Fluxo de Login.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

---

### **Fluxo de Ordenação**

### **CT010 - Ordenação por menor preço**

- **Descrição**: Validar a ordenação dos produtos pelo menor preço.
- **Pré-condições**: Produtos cadastrados com preços variados.
- **Passos para execução**:
    1. Acessar a página inicial “**Products”**
    2. Selecionar a opção “Menor preço” no filtro de ordenação.
- **Resultado esperado**: Produtos exibidos em ordem crescente de preço.
- **Suíte de teste**: Ordenação e Filtragem.
- **Ambiente**: Desktop.
- **Status**: Aprovado.

### **CT011 - Ordenação por maior preço**

- **Descrição**: Ordenação por maior preço.
- **Pré-condições**: Produtos cadastrados com preços variados.
- **Passos para execução**:
    1. Acessar a página inicial “**Products”**
    2. Selecionar a opção “Maior preço” no filtro de ordenação.
- **Resultado esperado**: Produtos exibidos em ordem decrescente de preço.
- **Suíte de teste**: Ordenação e Filtragem.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT012 - Ordenação por ordem alfabética crescente**

- **Descrição**: Validar a ordenação dos produtos em ordem alfabética crescente.
- **Pré-condições**: Produtos cadastrados com nomes variados.
- **Passos para execução**:
    1. Acessar a página inicial “**Products”**
    2. Selecionar a opção “A a Z” no filtro de ordenação.
- **Resultado esperado**: Produtos exibidos em ordem alfabética crescente.
- **Suíte de teste**: Ordenação e Filtragem.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT013 - Ordenação por ordem alfabética decrescente**

- **Descrição**: Validar a ordenação dos produtos em ordem alfabética decrescente.
- **Pré-condições**: Produtos cadastrados com nomes variados.
- **Passos para execução**:
    1. Acessar a página inicial “**Products”**
    2. Selecionar a opção “Z a A” no filtro de ordenação.
- **Resultado esperado**: Produtos exibidos em ordem alfabética decrescente.
- **Suíte de teste**: Ordenação e Filtragem.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

---

### **### Fluxo completo de compra (do carrinho até finalização)**

### **CT014 - Compra com sucesso**

- **Descrição**: Verificar o fluxo de compra do carrinho até a finalização do pedido.
- **Pré-condições**: Estar logado, 1 ou mais produtos adicionado ao carrinho.
- **Passos para execução**:
    1. Na tela do carrinho, clique o botão “Checkout”.
    2. Na tela do formulário, preencha os dados do cliente nos campos: “First name”, “Last name” e “zip/postal code”.
    3. Logo após o preenchimento, clique o botão “Continue”.
    4. Na tela “Checkout: Overview”, clique  o botão “Finish”.
- **Resultado esperado**: Deve aparecer a página de “Checkout: Complete!” com a mensagem de sucesso.
- **Suíte de teste**: Processo de Compra.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT015 - Carrinho vazio**

- **Descrição**: Compra sem sucesso com o carrinho sem nenhum produto adicionado.
- **Pré-condições**: Estar logado, nenhum produto adicionado no carrinho.
- **Passos para execução**:
    1. Na tela “Your Cart”, com o carrinho vazio, clique o botão “Checkout”.
- **Resultado esperado**: Deve aparecer alguma mensagem de erro e impedindo ir para próxima pagina.
- **Suíte de teste**: Processo de Compra.
- **Ambiente**: Desktop.
- **Status**: Reprovado.

### **CT016 - Formulário cliente vazio**

- **Descrição**: Formulário cliente com nenhum campo preenchido.
- **Pré-condições**: Estar logado, 1 ou mais produtos adicionado no carrinho.
- **Passos para execução**:
    1. Na tela “Your Cart”, clique no botão “Checkout”.
    2. Na tela do “Checkout: Your Information”, deixe todos os campos vazios e clique no botão “Continue”.
- **Resultado esperado**: Na página “**Checkout: Your Information**”, Deve aparecer alguma mensagem de erro e impedindo ir para próxima pagina.
- **Suíte de teste**: Processo de Compra.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT017 - Formulário cliente com o campo First name vazio**

- **Descrição**: Formulário cliente com o campo “First name” vazio.
- **Pré-condições**: Estar logado, 1 ou mais produtos  adicionado no carrinho.
- **Passos para execução**:
    1. Na tela “Your Cart”, clique no botão “Checkout”.
    2. Na tela do “Checkout: Your Information”, deixe somente o  campo “First name” vazio e preencha os demais campos e  clique no botão “Continue”.
- **Resultado esperado**: Na página “**Checkout: Your Information**”, Deve aparecer alguma mensagem de erro e impedindo ir para próxima pagina.
- **Suíte de teste**: Processo de Compra.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT018 - Formulário cliente com o campo Last name vazio**

- **Descrição**: Formulário cliente com o campo “Last name” vazio.
- **Pré-condições**: Estar logado, 1 ou mais produtos adicionado no carrinho.
- **Passos para execução**:
    1. Na tela “Your Cart”, clique no botão “Checkout”.
    2. Na tela do “Checkout: Your Information”, deixe somente o  campo “Last name” vazio e preencha os demais campos e  clique no botão “Continue”.
- **Resultado esperado**: Na página “**Checkout: Your Information**”, Deve aparecer alguma mensagem de erro e impedindo ir para próxima pagina.
- **Suíte de teste**: Processo de Compra.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT019 - Formulário cliente com o campo Postal Code vazio**

- **Descrição**: Formulário cliente com o campo “Postal Code” vazio.
- **Pré-condições**: Estar logado, 1 ou mais produtos adicionado no carrinho.
- **Passos para execução**:
    1. Na tela “Your Cart”, clique no botão “Checkout”.
    2. Na tela do “Checkout: Your Information”, deixe somente o  campo “Zip/Postal Code” vazio e preencha os demais campos e  clique no botão “Continue”.
- **Resultado esperado**: Na página “**Checkout: Your Information**”, Deve aparecer alguma mensagem de erro e impedindo ir para próxima pagina.
- **Suíte de teste**: Processo de Compra.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

---

### **Remoção de itens do carrinho**

### **CT020 - Remoção de todos os itens do carrinho**

- **Descrição**: Validar o comportamento ao remover todos os itens do carrinho.
- **Pré-condições**: Carrinho com múltiplos itens adicionados.
- **Passos para execução**:
    1. Acessar a página “**Your Cart”**.
    2. Remover todos os itens, um por vez, clicando no botão “Remove” de cada produto.
- **Resultado esperado**: O carrinho fica vazio.
- **Suíte de teste**: Fluxo de Remoção.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT021 - Remoção de item na página inicial**

- **Descrição**: Validar a remoção de um item diretamente na página inicial de produtos.
- **Pré-condições**: Carrinho com pelo menos um item adicionado da página inicial.
- **Passos para execução**:
    1. Acessar a página inicial “**Products”**.
    2. Localizar o produto que já está no carrinho.
    3. Clicar no botão “Remove” ao lado do produto.
- **Resultado esperado**: O produto é removido, e o contador do carrinho é atualizado corretamente.
- **Suíte de teste**: Fluxo de Remoção.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT022 - Remoção de item do carrinho**

- **Descrição**: Validar a remoção de um item específico do carrinho.
- **Pré-condições**: Carrinho com pelo menos um item adicionado.
- **Passos para execução**:
    1. Acessar a página “**Your Cart”**.
    2. Identificar o produto desejado na lista.
    3. Clicar no botão “Remove” associado ao produto.
- **Resultado esperado**: O produto é removido do carrinho, e o total é atualizado corretamente.
- **Suíte de teste**: Fluxo de Remoção.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

---

### **Navegação entre páginas**

### **CT023 - Acessar página de carrinho**

- **Descrição**: Validar a navegação para a página de carrinho ao clicar no ícone do carrinho.
- **Pré-condições**: Carrinho com itens adicionados.
- **Passos para execução**:
    1. Clicar no ícone de “Carrinho” no menu de navegação.
- **Resultado esperado**: Página “**Your Cart**” é carregada com os itens adicionados exibidos corretamente.
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT024 - Navegar para a página de checkout**

- **Descrição**: Validar a navegação para a página de checkout ao clicar no botão “Checkout” no carrinho.
- **Pré-condições**: Carrinho com itens adicionados.
- **Passos para execução**:
    1. Acessar a página “**Your Cart**”
    2. Clicar no botão “Checkout”.
- **Resultado esperado**: Página “**Checkout: Your Information”** é carregada corretamente.
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT025 - Acessar página de resumo da compra**

- **Descrição**: Validar a navegação d a pagina “**Checkout: Your Information**” para pagina “**Checkout: Overview**”.
- **Pré-condições**: Dados do cliente preenchidos corretamente.
- **Passos para execução**:
    1. Preencher os campos “First Name”, “Last Name” e “Zip/Postal Code” na página “**Checkout: Your Information”**.
    2. Clicar no botão “Continue”.
- **Resultado esperado**: Página “**Checkout: Overview”** é carregada com informações corretas do pedido.
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT026 - Navegar para a página de confirmação do pedido**

- **Descrição**: Validar a navegação para a “**Checkout: Complete!”** ao finalizar a compra.
- **Pré-condições**: Esta na pagina  “**Checkout: Overview”**
- **Passos para execução**:
    1. Acessar a página “**Checkout: Overview”**
    2. Clicar no botão “Finish”.
- **Resultado esperado**: Página “**Checkout: Complete!”** é carregada.
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT027 - Navegar da página de confirmação de pedido para tela de home**

- **Descrição**: Navegar da página “**Checkout: Complete!”** para a tela inicial “**Products”**
- **Pré-condições**: Está na tela de “Checkout: Complete!”.
- **Passos para execução**:
    1. Clicar no botão “Back Home”.
- **Resultado esperado**: Página “**Products”** é carregada.
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT028 - Navegar da página Your Cart para a página Products**

- **Descrição**: Retroceder da página Your Cart para a página Products.
- **Pré-condições**: Está na página Your Cart.
- **Passos para execução**:
    1. Clicar no botão “Continue Shopping”.
- **Resultado esperado**: O usuário é redirecionado para a página principal “**Products”**
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT029 - Navegar da página Checkout: Your Information para Your Cart**

- **Descrição**: Retroceder da página “Checkout: Your Information” para “Your Cart.”
- **Pré-condições**: Está na página Checkout: Your Information.
- **Passos para execução**:
    1. Clicar no botão “Cancel”.
- **Resultado esperado**: O usuário é redirecionado para a página principal com Your Cart.
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT030 - Navegar da página Checkout: Overview Information para Checkout: Your Information**

- **Descrição**: Retroceder da página Checkout: Overview Information para Checkout: Your Information.
- **Pré-condições**: Está na página Checkout: Overview Information.
- **Passos para execução**:
    1. Clicar no botão “Cancel”.
- **Resultado esperado**: O usuário é redirecionado para a página Checkout: Your Information.
- **Suíte de teste**: Navegação.
- **Ambiente**: Desktop.
- **Status**: Reprovado.

---

### **Fluxo de Logout**

### **CT031 - Realizando Logout**

- **Descrição**: Validar que o usuário é desconectado com sucesso ao acionar o botão “Logout”.
- **Pré-condições**: Usuário está logado na aplicação.
- **Passos para execução**:
    1. Acessar o menu de navegação.
    2. Clicar no botão “Logout”.
- **Resultado esperado**: Sessão encerrada e redirecionamento para a página de login.
- **Suíte de teste**: Fluxo de Logout.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.

### **CT032 - Acesso após sessão encerrada**

- **Descrição**: Validar que o sistema impede acesso a páginas autenticadas após o logout.
- **Pré-condições**: Sessão encerrada.
- **Passos para execução**:
    1. Tentar retroceder a página clicando no botão de voltar do navegador.
- **Resultado esperado**: Deve aparecer alguma mensagem de erro e impedindo retroceder pagina.
- **Suíte de teste**: Fluxo de Logout.
- **Ambiente**: Desktop.
- **Status**:  Aprovado.


## 7. Ferramentas e Recursos

- **Ferramentas de Teste**:
	- Notion (Versão 2.46)
	- Google Chrome (Versão 131.0.6778.86)
	- Visual Studio Code (Versào: 1.95.3)
	- https://markdown.net.br/editor/
- **Ambiente de Teste**: Windows 11.


## 8. Cronograma

| Atividade                | Responsável          | Data de Início | Data de Término |
|--------------------------|----------------------|----------------|-----------------|
| Planejamento dos testes  | Matheus Gama         | 23/11/2024     | 23/11/2024      |
| Execução dos casos de teste | Matheus Gama       | 23/11/2024     | 23/11/2024      |



## 9. Análise de riscos da aplicação

### Riscos
- A plataforma pode apresentar indisponibilidade temporária devido a manutenções programadas ou alta demanda de acessos, impactando diretamente a execução dos testes.
- Atualizações ou modificações no e-commerce Sauce Demo, realizadas sem aviso prévio, podem alterar elementos da interface ou funcionalidades, resultando em falhas nos casos de testes e no plano de testes.

### Dependências 
- Acesso estável à internet: A execução dos testes depende de uma conexão de internet confiável para acessar o Sauce Demo. Qualquer instabilidade pode comprometer a continuidade do processo de teste.
- Credenciais de acesso: É necessário o fornecimento de credenciais válidas para realizar os testes com sucesso.

## 10. Resultados dos Testes Executados

## Detalhamento dos Resultados

| ID do Caso de Teste | Descrição | Resultado | Observação |
|---------------------|--------------|-----------|----------------|
| CT001              | Testar login com credenciais do usuário “standard_user”. | Aprovado | N/A |
| CT002              | Testar login com credenciais do usuário “locked_out_user”. | Reprovado | Ao executar o teste conforme o CT002, aparece a seguinte mensagem de erro na tela de login: "Epic sadface: Sorry, this user has been locked out."  impossibilitado o login. |
| CT003              | Testar login com credenciais do usuário “problem_user”. | Aprovado | Após o login, as imagem do produto estão repetidas |
| CT004               | Testar login com credenciais do usuário “performance_glitch_user”. | Aprovado | Após executar o teste CT004, ao clicar no botão "login", a tela inicial do produtos aparecer após 5 segundos.  |
| CT005              | Testar login com credenciais do usuário “error_user”. | Aprovado | N/A |
| CT006              | Testar login com credenciais do usuário “visual_user”. | Aprovado | O botão item do 'Carrinho' e o botão 'Add to cart' estão desalinhados, aparecendo fora da posição esperada na interface na pagina Products. |
| CT007              | Testar login com credenciais inválidas. | Aprovado | N/A |
| CT008              | Testar login com o campo de usuário vazio. | Aprovado | N/A |
| CT009              | Testar login com o campo de senha vazio. | Aprovado | N/A |
| CT010              |  Validar a ordenação dos produtos pelo menor preço. | Aprovado | N/A |
| CT011              | Validar a ardenação por maior preço. | Aprovado | N/A |
| CT012              | Validar a ordenação dos produtos em ordem alfabética crescente.| Aprovado | N/A |
| CT013              | Validar a ordenação dos produtos em ordem alfabética decrescente.| Aprovado | N/A |
| CT014              | Verificar o fluxo de compra do carrinho até a finalização do pedido.| Aprovado | N/A |
| CT015              | Compra sem sucesso com o carrinho sem nenhum produto adicionado.| Reprovado | O sistema permite concluir uma compra mesmo com o carrinho vazio, sem nenhum produto selecionado |
| CT016              | Formulário cliente com nenhum campo preenchido.| Aprovado | N/A |
| CT017              | Formulário cliente com o campo “First name” vazio.| Aprovado | N/A |
| CT018              | Formulário cliente com o campo “Last name” vazio. | Aprovado | N/A |
| CT019              | Formulário cliente com o campo “Zip/Postal Code” vazio. | Aprovado | N/A |
| CT020              | Validar o comportamento ao remover todos os itens do carrinho. | Aprovado | N/A |
| CT021              | Validar a remoção de um item diretamente na página inicial de produtos. | Aprovado | N/A |
| CT022              | Validar a remoção de um item específico do carrinho. | Aprovado | N/A |
| CT023              | Validar a navegação para a página de carrinho ao clicar no ícone do carrinho. | Aprovado | N/A |
| CT024              | Validar a navegação para a página de checkout ao clicar no botão “Checkout” no carrinho. | Aprovado | N/A |
| CT025              | Validar a navegação d a pagina “Checkout: Your Information” para pagina “Checkout: Overview”. | Aprovado | N/A |
| CT026              | Validar a navegação da pagina “Checkout: Your Information” para pagina “Checkout: Overview”. | Aprovado | N/A |
| CT027              | Navegar da página “Checkout: Complete!” para a tela inicial “Products” | Aprovado | N/A |
| CT028              | Retroceder da página Your Cart para a página Products. | Aprovado | N/A |
| CT029              |Retroceder da página “Checkout: Your Information” para “Your Cart.” | Aprovado | N/A |
| CT030              | Retroceder da página Checkout: Overview Information para Checkout: Your Information. | Reprovado	 | A aplicação não permite que o usuário volte da pagina Checkout: Overview Information para pagina Checkout: Your Information. |
| CT031              | Validar que o usuário é desconectado com sucesso ao acionar o botão “Logout”. | Aprovado		 | N/A |
| CT032             | Validar que o sistema impede acesso a páginas autenticadas após o logout. | Aprovado		 | N/A |


## 11. Lista de Bugs Encontrados

| ID do Bug | Descrição | Impacto | Status | Observação |
|-----------|--------------|---------|--------|----------------|
| BUG-001   | usuário "locked_out_user" com login Bloqueado | [Médio] | [Aberto] | Ao executar o teste conforme o CT002, aparece a seguinte mensagem de erro na tela de login: "Epic sadface: Sorry, this user has been locked out." impossibilitado o login. |
| BUG-002   | Compra sem sucesso com o carrinho sem nenhum produto adicionado. | [Alto] | [Aberto] | O sistema permite concluir uma compra mesmo com o carrinho vazio, sem nenhum produto selecionado |
| BUG-003   | Retroceder da página Checkout: Overview Information para Checkout: Your Information. | [Baixo] | [Aberto] | A aplicação não permite que o usuário volte da pagina Checkout: Overview Information para pagina Checkout: Your Information. |

## 12. Sugestões de melhorias

- Na página "Your Cart", adicionar uma mensagem informando que o carrinho está vazio para orientar o usuário.
- Na página "Checkout: Your Information", ajustar a validação dos campos "First Name" e "Last Name" para impedir a inserção de números.
- Implementar validação no campo "Zip/Postal Code" para aceitar apenas valores numéricos ou formatos válidos.
- Na página "Checkout: Overview", incluir as informações do cliente coletadas anteriormente, tornando o resumo do pedido mais completo e claro.
- Garantir que as mensagens de erro sejam claras, objetivas e orientem o usuário na correção dos problemas.
- Resolver os bugs específicos relatados:
	- Corrigir a exibição de imagens dos produtos após o login com o usuário "problem_user".
	- Garantir o funcionamento correto de todos os botões "ADD TO CART" na pagina “Products”.
	- Ajustar o cálculo do valor final do pedido.
	- Melhorar o desempenho para o usuário "performance_glitch_user", reduzindo a latência no login e na navegação entre páginas.
    Adicionar novas funcionalidades para tornar a aplicação mais semelhante a um e-commerce do mundo real.

**Impactos Negativos:**

Esses erros têm o potencial de gerar frustração, reduzir a confiança no sistema e levar usuários a abandonar o uso da aplicação. 
Melhorar o processamento de pedidos, oferecer mensagens claras e otimizar a performance são algumas sugestões que pode transformar a experiência do usuário,
 aumentando a satisfação e a reputação do e-commerce Sauce Demo .


## 13. Sugestões de automação

- Automatizar o login de diferentes tipos de usuários para garantir que, de forma automática, cada perfil tenha o comportamento e as permissões corretas .
- Automatizar as mensagens de erro no login, para que, automaticamente, o sistema apresente mensagens claras e úteis ao usuário, caso haja erros nas credenciais ou campos obrigatórios em branco.
- Automatizar a verificação da exibição dos produtos no carrinho, garantindo que os itens adicionados apareçam corretamente, para que o usuário tenha total visibilidade do que está comprando.
- Automatizar a remoção de itens do carrinho e a atualização do total de forma precisa e imediata, sem que o usuário precise realizar nenhuma ação adicional.
- Automatizar a validação do processo de checkout, desde o preenchimento das informações do cliente até a confirmação do pedido, para que todas as etapas sejam verificadas automaticamente e sem falhas no fluxo de compra.
- Automatizar a checagem do resumo do pedido, garantindo que todos os itens e valores sejam conferidos automaticamente antes da finalização da compra, evitando qualquer erro.
- Automatizar os testes de botões e links de navegação (como "ADD TO CART", "REMOVE"), garantindo que o sistema teste de forma contínua se esses elementos estão funcionando corretamente, oferecendo uma navegação fluida ao usuário sem falhas.
- Automatizar a validação da navegação entre as páginas principais (Products, Your Cart, Checkout: Your Information, Checkout: Overview, Checkout: Complete), para assegurar que o sistema sempre verifique se a navegação está ocorrendo sem interrupções.

