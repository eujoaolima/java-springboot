# Spring MVC

É um framework que facilita o desenvolvimento de aplicações web. Baseado no paradigma MVC torna possível a construção de web services.

# Model View Controller (MVC)

É um padrão de arquitetura de software com o objetivo de separar os conceitos em três camadas interconectadas.

    ## Estruturação:
        -> Controle é a camada de ação, onde são manipulados os dados que o usuário insere ou atualiza, chamando em seguida o Modelo.

        -> Modelo permite o acesso aos dados que serão coletados, gravados e exibidos.

        -> Visão pode ser qualquer saída de representação dos dados, como uma tabela ou uma página.

    ### Exemplo:

            @Controller
            public class HelloController {

                @RequestMapping(value="/", method= RequestMethod.GET)
                @ResponseBody
                public String hello() {
                    return "Hello World!";
                }
            }