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
  import Controller.UserController;
  import View.UserView;
  import Model.User;

  import java.util.List;

  public class Main {
      public static void main(String[] args) {
          UserController controller = new UserController();
          UserView view = new UserView();

          List<User> usuarios = controller.listarUsuarios();
          view.mostrarUsuarios(usuarios);
      }
  }

<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
         http://maven.apache.org/xsd/maven-4.0.0.xsd">

    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>neon-db-test</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
    </properties>

    <dependencies>

        <dependency>
            <groupId>org.postgresql</groupId>
            <artifactId>postgresql</artifactId>
            <version>42.7.3</version>
        </dependency>

        <dependency>
            <groupId>org.openjfx</groupId>
            <artifactId>javafx-controls</artifactId>
            <version>21.0.2</version>
        </dependency>


        <!-- JavaFX controls -->
        <dependency>
            <groupId>org.openjfx</groupId>
            <artifactId>javafx-controls</artifactId>
            <version>21.0.2</version>
        </dependency>

        <!-- JavaFX graphics -->
        <dependency>
            <groupId>org.openjfx</groupId>
            <artifactId>javafx-graphics</artifactId>
            <version>21.0.2</version>
        </dependency>

        <dependency>
            <groupId>org.openjfx</groupId>
            <artifactId>javafx-controls</artifactId>
            <version>21.0.2</version>
            <classifier>linux</classifier>
        </dependency>

    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-dependency-plugin</artifactId>
                <version>3.6.1</version>
                <executions>
                    <execution>
                        <id>copy-dependencies</id>
                        <phase>package</phase>
                        <goals>
                            <goal>copy-dependencies</goal>
                        </goals>
                        <configuration>
                            <outputDirectory>${project.build.directory}/lib</outputDirectory>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>


</project>
