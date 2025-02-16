# 📦 E-commerce Database Schema 

## 📌 Descrição do Projeto  
Este projeto representa o **modelo conceitual e relacional** de um sistema de **e-commerce**, permitindo o gerenciamento de **clientes, pedidos, pagamentos, estoque e entregas**. O banco de dados foi estruturado para garantir **eficiência, integridade dos dados e escalabilidade**.  
Modelo entidade relacionamento de um banco de dados de e-commerce proposto no bootcamp da Dio.

## 🏗️ Estrutura do Banco de Dados  
O banco de dados segue um **modelo relacional**, composto por múltiplas tabelas interconectadas para garantir um fluxo consistente de informações.  

### **📊 Principais Entidades e Relacionamentos**  

1. **Cliente**  
   - Se divide em **Pessoa Física (Cliente_PF)** e **Pessoa Jurídica (Cliente_PJ)**.  
   - Um cliente pode realizar múltiplos pedidos (**1:N**).  

2. **Pedido**  
   - Associado a um único cliente (**1:N**).  
   - Pode conter múltiplos produtos (**N:N**, gerenciado pela tabela `Itens_Pedido`).  
   - Está vinculado a um pagamento (**1:1**) e a uma entrega (**1:1**).  

3. **Produto**  
   - Presente em múltiplos pedidos (**N:N** via `Itens_Pedido`).  
   - Controlado pelo estoque (**1:N** com `Estoque`).  
   - Pode ser fornecido por vários fornecedores (**N:N** via `Disponibilidade_Produto`).  

4. **Pagamento**  
   - Relacionado a um único pedido (**1:1**).  
   - Possui informações sobre o método de pagamento e status.  

5. **Entrega**  
   - Associada a um único pedido (**1:1**).  
   - Possui status e código de rastreio.  

6. **Estoque**  
   - Controla a disponibilidade dos produtos.  
   - Relaciona-se com **Produto** (**1:N**).  

7. **Fornecedor**  
   - Pode fornecer múltiplos produtos (**N:N** via `Disponibilidade_Produto`).  

## 🔗 Modelo Relacional  
Abaixo estão os principais relacionamentos do banco de dados:  

- **Cliente_PF / Cliente_PJ** → Pedido (**1:N**)  
- **Pedido** → Produto (**N:N** via `Itens_Pedido`)  
- **Pedido** → Pagamento (**1:1**)  
- **Pedido** → Entrega (**1:1**)  
- **Produto** → Estoque (**1:N**)  
- **Produto** → Fornecedor (**N:N** via `Disponibilidade_Produto`)  

## 🎯 Objetivo do Projeto  
Este banco de dados foi modelado para atender às necessidades de um **e-commerce** de forma eficiente, garantindo:  
✅ Controle de pedidos e clientes.  
✅ Gerenciamento de pagamentos e entregas.  
✅ Monitoramento do estoque e fornecedores.  
✅ Relacionamentos otimizados para escalabilidade.  

## 🚀 Tecnologias Utilizadas  
- **MySQL** 
- **Diagramação com MySQL Workbench** 
