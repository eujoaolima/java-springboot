# Anotações Hibernate

@Entity: É utilizada para mapear a classe que será uma entidade. A partir disso, a classe estabelecerá uma ligação a uma tabela em um banco de dados.

    Exemplo:

        @Entity
        public class Produto {
            ...
        }

@Table: É utilizada para acompanhar a anotação @Entity. Por meio dele, podemos definir o nome da tabela que será gerada.

    Exemplo:

        @Entity
        @Table(name = 'produtos')
        public class Produto {
            ...
        }

@Id: É utilizada para mapear a propriedade que será chave primária da tabela. Define o campo de identificação único para cada registro.

    Exemplo:

            @Entity
            @Table(name = 'produtos')
            public class Produto {
                @Id
                private Long id;
                ...
            }

@Column: É uma anotação opcional que pode acompanhar a propriedade do objeto. Ele permite definir algumas características do campo como nome, nulidade e tamanho.

    Exemplo:

        @Entity
        @Table(name = 'produtos')
        public class Produto {
            @Id
            private Long id;

            @Column(name= 'desc', nullable = false, length = 200)
            private String descricao;
        }

@OneToOne: É utilizada para estabelecer um relacionamento um-para-um.

    Exemplo:

        @Entity
        @Table(name = 'produtos')
        public class Produto {
            @Id
            private Long id;

            @Column(name= 'desc', nullable = false, length = 200)
            private String descricao;

            @OneToOne
            private Codigo codigo;
        }

@ManyToOne: É utilizada para estabelecer um relacionamento muitos-para-um.

    Exemplo:

        @Entity
        @Table(name = 'produtos')
        public class Produto {
            @Id
            private Long id;

            @Column(name= 'desc', nullable = false, length = 200)
            private String descricao;

            @ManyToOne
            private Lote lote;
        }

@ManyToMany: É utilizada para estabelecer um relacionamento muitos-para-muitos.

    Exemplo:

        @Entity
        @Table(name = 'produtos')
        public class Produto {
            @Id
            private Long id;

            @Column(name= 'desc', nullable = false, length = 200)
            private String descricao;

            @ManyToMany
            private List<Item> itens;
        }