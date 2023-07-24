# O que é Spring?

Spring é um conjunto de frameworks focados na facilitação em construção de aplicações em Java. No seu ecossistema, podem ser destacados:
    - Spring Framework: Fornece um modelo abrangente de programação e configuração para aplicativos baseados em Java. Os outros modelos de programação Spring sempre acabam sendo centralizados no Spring Framework.
    
    - Spring Boot:É um framework que torna configuração e inicialização de aplicações Spring automáticas, possibilitando a execução imediata. Para configurar uma aplicação com Spring Boot, utilizamos anotações (recursos nativos da linguagem usados para marcar classes, propriedades e métodos, garantindo as características do Spring).

        Exemplo:
            import org.springframework.boot.SpringApplication;
            import org.springframework.boot.autoconfigure.SpringBootApplication;

            @SpringBootApplication
            public class MyClass {
                public static void main(String[] args) {
                    SpringApplication.run(MyClass.class, args);
                }
            }

    - Spring Data: fornece um modelo de programação baseado em Spring para o acesso e manipulação de dados.

    - Spring MVC: É um framework que nos auxilia no desenvolvimento de web services. Com ele, é possível ter praticidade para trabalhar com requisições web.

    - Spring Security: É uma estrutura de autenticação e controle de acesso. É o padrão para proteger aplicativos baseados em Spring.
