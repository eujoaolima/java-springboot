# DI & IoC - Injeção de Dependências e Inversão de Controle

- Dependency Injection (DI): É uma prática em que os objetos são projetados de maneira que suas instâncias sejam injetadas ao invés de construí-las internamente.

- Inversion of Control (IoC): É um princípio de desenvolvimento onde o controle de chamadas dos objetos é definido por uma estrutura de software.

Exemplo:

### Utilização sem injeção de dependência
    public class ProdutoController {
        private ProdutoService service = new ProdutoService();
        ...
    }

### Utilização com injeção de dependência
    @Controller
    public class ProdutoController {
        @Autowired
        private ProdutoService service;
        ...
    }

    @Autowired é a anotação utilizada para aplicar injeção de dependência. Ele permite que o Spring seja a estrutura de software responsável pela instância do objeto.