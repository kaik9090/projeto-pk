# projeto-pk
# Projeto Final - Atividade em Grupo

## Descrição
Este é um projeto final de desenvolvimento de sistema CRUD utilizando **Java**, **PostgreSQL** e **GitHub**. O objetivo do projeto é criar um sistema simples de gerenciamento de usuários, onde podemos realizar operações de **Create**, **Read**, **Update** e **Delete**.

## Funcionalidades
- Inserir novos usuários no banco de dados.
- Listar todos os usuários cadastrados.
- Atualizar informações de um usuário.
- Excluir um usuário do banco de dados.

## Tecnologias Utilizadas
- **Java** (JDBC)
- **PostgreSQL** (Banco de Dados)
- **GitHub** (Controle de versão)
- **Maven** (Gerenciamento de dependências)

## Como Executar o Projeto

### Pré-requisitos
- JDK 11 ou superior
- Maven
- Banco de Dados PostgreSQL configurado (pode utilizar Neon Console ou outra plataforma)

### Passos para Execução
1. Clone este repositório:

   ```bash
   git clone https://github.com/seu-usuario/projeto-final-grupo.git

   nome projeto-final-grupo 
  
  <dependencies>
    <dependency>
        <groupId>org.postgresql</groupId>
        <artifactId>postgresql</artifactId>
        <version>42.2.23</version>
    </dependency>
  </dependencies>
  import java.sql.*;

  public class Main {
    public static void main(String[] args) {
        // Configurações do banco de dados (substitua pelos dados do Neon Console)
        String url = "jdbc:postgresql://<HOST>:<PORT>/<DB_NAME>";
        String username = "<USER>";
        String password = "<PASSWORD>";

        try {
            // Conexão com o banco de dados
            Connection conn = DriverManager.getConnection(url, username, password);

            // Exemplo de operação CRUD (CREATE)
            String insertSQL = "INSERT INTO usuarios (nome, email, senha) VALUES (?, ?, ?)";
            PreparedStatement stmt = conn.prepareStatement(insertSQL);
            stmt.setString(1, "Maria Souza");
            stmt.setString(2, "maria@exemplo.com");
            stmt.setString(3, "senha456");

            int rowsAffected = stmt.executeUpdate();
            System.out.println("Número de linhas inseridas: " + rowsAffected);

            // Operação READ
            String selectSQL = "SELECT * FROM usuarios";
            Statement selectStmt = conn.createStatement();
            ResultSet rs = selectStmt.executeQuery(selectSQL);

            while (rs.next()) {
                int id = rs.getInt("id");
                String nome = rs.getString("nome");
                String email = rs.getString("email");
                System.out.println("ID: " + id + ", Nome: " + nome + ", E-mail: " + email);
            }

            // Fechar a conexão
            conn.close();

        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
  }
import java.sql.*;

public class Main {
    public static void main(String[] args) {
        // Configurações do banco de dados (substitua pelos dados do Neon Console)
        String url = "jdbc:postgresql://<HOST>:<PORT>/<DB_NAME>";
        String username = "<USER>";
        String password = "<PASSWORD>";

        try {
            // Conexão com o banco de dados
            Connection conn = DriverManager.getConnection(url, username, password);

            // Operação CREATE: Inserir um novo usuário no banco
            String insertSQL = "INSERT INTO usuarios (nome, email, senha) VALUES (?, ?, ?)";
            PreparedStatement insertStmt = conn.prepareStatement(insertSQL);
            insertStmt.setString(1, "Maria Souza");
            insertStmt.setString(2, "maria@exemplo.com");
            insertStmt.setString(3, "senha456");

            int rowsAffected = insertStmt.executeUpdate();
            System.out.println("Número de linhas inseridas: " + rowsAffected);

            // Operação READ: Buscar todos os usuários cadastrados
            String selectSQL = "SELECT * FROM usuarios";
            Statement selectStmt = conn.createStatement();
            ResultSet rs = selectStmt.executeQuery(selectSQL);

            // Exibir os usuários no console
            System.out.println("Usuários cadastrados:");
            while (rs.next()) {
                int id = rs.getInt("id");
                String nome = rs.getString("nome");
                String email = rs.getString("email");
                System.out.println("ID: " + id + ", Nome: " + nome + ", E-mail: " + email);
            }

            // Fechar a conexão
            conn.close();

        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}

