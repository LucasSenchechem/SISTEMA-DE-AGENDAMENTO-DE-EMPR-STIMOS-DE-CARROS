# Arquitetura do Sistema

O Sistema de Agendamento de Empréstimos de Carros foi projetado utilizando uma arquitetura em camadas, seguindo o modelo cliente-servidor, com acesso por meio de navegadores web.

Essa organização tem como objetivo separar as responsabilidades do sistema, facilitando seu desenvolvimento, manutenção e futuras atualizações.

<img width="1280" height="1229" alt="image" src="https://github.com/user-attachments/assets/b6e61ad4-7b13-4b88-b98b-5e640e5c1c52" />

### Camada de Apresentação

Responsável pela interação entre os usuários e o sistema.

Contempla as interfaces utilizadas pelos clientes e funcionários para consultar veículos, realizar aluguéis, gerenciar cadastros e registrar devoluções.

Também recebe as solicitações dos usuários e encaminha as operações para a camada de negócio.

### Camada de Negócio

Responsável pelo processamento das funcionalidades e pela aplicação das regras de negócio.

É composta pelos gerenciadores de veículos, clientes, funcionários e aluguéis.

Entre suas responsabilidades estão verificar a disponibilidade dos veículos, impedir aluguéis duplicados, validar os cadastros e controlar o processo de locação e devolução.

### Camada de Persistência

Responsável pelo armazenamento e recuperação das informações.

Utiliza repositórios para realizar a comunicação com um banco de dados relacional, armazenando os registros de veículos, clientes e aluguéis.

Essa camada busca garantir a integridade, a consistência e a persistência dos dados.

### Fluxo de Funcionamento

O funcionamento do sistema segue o seguinte processo:

1. O usuário realiza uma ação na interface.
2. A camada de apresentação recebe a solicitação.
3. A camada de negócio verifica as regras e processa a operação.
4. A camada de persistência consulta ou atualiza os dados necessários.
5. O resultado retorna para a interface e é apresentado ao usuário.

### Princípios Arquiteturais

O projeto considera os seguintes princípios de Engenharia de Software:

- **Separação de responsabilidades:** cada camada possui funções específicas.
- **Encapsulamento:** os dados são manipulados por operações controladas.
- **Baixo acoplamento:** busca reduzir a dependência entre os componentes.
- **Alta coesão:** cada classe concentra funcionalidades relacionadas à sua responsabilidade.
- **Manutenibilidade:** a organização facilita correções e futuras melhorias.
- **Integridade dos dados:** operações de aluguel devem manter as informações consistentes, evitando registros conflitantes.

Essa arquitetura foi definida para oferecer uma estrutura organizada, confiável e preparada para a evolução do sistema.
