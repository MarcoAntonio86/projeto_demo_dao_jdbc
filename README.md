#Projeto: Implementação de DAO com Factory e MySQL em Java

O projeto "Projeto Demo DAO JDBC" demonstra a implementação do padrão Data Access Object (DAO) em Java, utilizando o padrão Factory para a criação de instâncias e o MySQL Community Server como banco de dados. O objetivo é exemplificar a separação da lógica de acesso a dados da lógica de negócios, promovendo um design mais modular e de fácil manutenção.

📌 Funcionalidades Principais

Operações CRUD: Implementação das operações de criação, leitura, atualização e exclusão para as entidades Seller e Department.

Consultas Específicas:

findById: Busca uma entidade pelo seu identificador único.

findByDepartment: Recupera todos os vendedores associados a um determinado departamento.

🛠️ Tecnologias Utilizadas

Java: Linguagem de programação principal do projeto.

JDBC (Java Database Connectivity): API para conexão e execução de operações no banco de dados.

MySQL Community Server: Sistema de gerenciamento de banco de dados relacional utilizado.

Padrão DAO: Para abstração e encapsulamento do acesso a dados.

Padrão Factory: Para gerenciamento da criação de instâncias dos DAOs.

📂 Estrutura do Projeto
O projeto está organizado da seguinte forma:

graphql
Copiar
Editar
projeto_demo_dao_jdbc
├── src
│   ├── application
│   │   └── Program.java       # Classe principal para execução da aplicação
│   ├── db
│   │   ├── DB.java            # Gerenciamento da conexão com o banco de dados
│   │   └── DbException.java   # Classe para exceções relacionadas ao banco de dados
│   ├── model
│   │   ├── entities
│   │   │   ├── Department.java  # Entidade Department
│   │   │   └── Seller.java      # Entidade Seller
│   │   ├── dao
│   │   │   ├── DepartmentDao.java       # Interface DAO para Department
│   │   │   ├── SellerDao.java           # Interface DAO para Seller
│   │   │   ├── DaoFactory.java          # Factory para criação dos DAOs
│   │   │   └── impl
│   │   │       ├── DepartmentDaoJDBC.java  # Implementação JDBC do DAO de Department
│   │   │       └── SellerDaoJDBC.java      # Implementação JDBC do DAO de Seller
│   └── util
│       └── DataUtil.java         # Utilitário para manipulação de datas
├── db.properties                 # Arquivo de configuração do banco de dados
├── .classpath                    # Arquivo de configuração do classpath do projeto
├── .project                      # Arquivo de configuração do projeto
└── README.md                     # Documentação do projeto

🚀 Como Executar o Projeto
Pré-requisitos:

Java Development Kit (JDK) instalado.
MySQL Community Server instalado e em execução.
Configuração do Banco de Dados:

Crie um banco de dados chamado coursejdbc.
Execute os scripts SQL fornecidos para criar as tabelas necessárias.
Configuração da Aplicação:

Atualize o arquivo db.properties com as credenciais do seu banco de dados:
ini
Copiar
Editar
user=seu_usuario
password=sua_senha
dburl=jdbc:mysql://localhost:3306/coursejdbc
useSSL=false
Execução:

Compile e execute a classe Program.java localizada em src/application.

📌 Melhorias Futuras
Implementação de Testes Unitários: Adicionar testes para garantir a integridade das operações CRUD.
Tratamento de Exceções Aprimorado: Melhorar o manejo de exceções para cobrir mais cenários de erro.
Refatoração para Padrão MVC: Organizar o projeto seguindo o padrão Model-View-Controller para uma melhor separação de responsabilidades.


