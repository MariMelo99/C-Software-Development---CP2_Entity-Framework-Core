Integrantes do Grupo
Irana Pereira – RM98593
Lucas Vinicius Candido – RM98480
Mariana Melo – RM98121
Mateus Iago Sousa – RM550270
Turma: 3ESPV

Aplicação Console (.NET 8) + Entity Framework Core + Oracle

<img width="120" alt="MariMelo99" src="https://github.com/MariMelo99.png">

Descrição
Este projeto é uma aplicação Console em .NET 8 que utiliza Entity Framework Core com Oracle para realizar operações CRUD sobre a tabela TB_CLIENTE.
Importante: O projeto não utiliza Code-First nem Migrations. O banco já existe e o mapeamento é feito por atributos ([Table], [Column]). O script SQL para criação da tabela está disponível no repositório.

Requisitos Técnicos
.NET SDK: 8.0+
Oracle: 19c+ (ou compatível com ODP.NET Managed)
IDE recomendada: Visual Studio 2022
Acesso ao banco: host, porta (1521), service name (ex.: ORCL/XEPDB1), usuário e senha

Pacotes NuGet Utilizados
Microsoft.EntityFrameworkCore (8.*)
Oracle.EntityFrameworkCore (8.*)

Estrutura do Projeto
Model/Cliente.cs → Entidade com [Table]/[Column]
Model/Pedido.cs → Entidade com relacionamento para Cliente
DBContext/AppDbContext.cs → Contexto EF Core
Program.cs → Console App com menu CRUD (Clientes e Pedidos)
Scripts/TB_CLIENTE.sql → Script de criação da tabela

Script de Banco de Dados
O repositório contém o script SQL para criação manual da tabela TB_CLIENTE.
Esse script deve ser executado no schema do usuário configurado na connection string antes de rodar a aplicação.

## 📸 Prints de Execução
### Menu Principal
<img src="https://github.com/user-attachments/assets/c08856e4-d340-48fe-b395-4bed96a04548" width="600">
### Exemplo de Listagem de Clientes
<img src="https://github.com/user-attachments/assets/86fc9c29-8e82-4ba7-adfb-811dff894e57" width="600">


Como Executar
Garanta que a tabela TB_CLIENTE exista (rode o script do repositório).

Compile o projeto:
dotnet build
dotnet run

