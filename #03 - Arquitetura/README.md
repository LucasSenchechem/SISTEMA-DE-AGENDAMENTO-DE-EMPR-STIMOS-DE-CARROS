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
<img width="2720" height="2400" alt="fluxo_realizar_aluguel_sequencia" src="https://github.com/user-attachments/assets/f3322a4a-7545-45d2-9d1a-15b5e16f7c12" />


### Princípios Arquiteturais

O projeto considera os seguintes princípios de Engenharia de Software:

- **Separação de responsabilidades:** O sistema foi organizado de modo que a
interface com o usuário, as regras de negócio e o armazenamento dos dados
possuam responsabilidades distintas. A camada de apresentação recebe as
solicitações dos usuários, a camada de negócio processa as operações e verifica as
regras estabelecidas, enquanto a camada de persistência realiza o acesso ao banco
de dados. Essa separação facilita a compreensão e a manutenção do sistema.

- **Encapsulamento:** Os dados e comportamentos das entidades deverão ser
organizados de maneira que alterações importantes ocorram por meio de operações
controladas. Por exemplo, a disponibilidade de um veículo não deverá ser
modificada livremente pela interface, mas por operações que respeitem as regras de
negócio. Isso contribui para evitar alterações indevidas e inconsistências nas
informações.
- **Princípio da Responsabilidade Única (SRP):** Cada classe ou componente deverá
possuir uma responsabilidade principal. Por exemplo, a classe GerenciaVeiculo será
responsável pelas operações relacionadas aos veículos, enquanto GerenciaCliente
tratará das informações dos clientes. Já GerenciaAluguel coordena os processos de
locação e devolução, evitando concentrar diferentes funcionalidades em uma única
classe.
- **Abstração e Inversão de Dependências:** A camada de negócio utilizará interfaces
de repositório para consultar e armazenar informações, sem depender diretamente
de uma tecnologia específica de banco de dados. Dessa forma, será possível
modificar a implementação da persistência sem alterar as principais regras de
negócio do sistema.

- **Simplicidade e Reutilização:** Serão considerados os princípios KISS (Keep It
Simple) e DRY (Don't Repeat Yourself), buscando soluções simples e evitando a
duplicação desnecessária de regras e funcionalidades. Por exemplo, a verificação
da disponibilidade de um veículo deverá ser centralizada na lógica de negócio, em
vez de ser implementada separadamente em diferentes telas.

- **Integridade dos dados:** As operações deverão respeitar as regras
de negócio definidas anteriormente. Durante a realização de um aluguel, o registro
da locação e a atualização da disponibilidade do veículo deverão ocorrer em uma
única transação. Caso alguma etapa falhe, nenhuma alteração deverá ser
confirmada, evitando que um veículo seja alugado simultaneamente para mais de
um cliente.
A aplicação desses princípios tem como objetivo produzir um projeto organizado,
compreensível e preparado para futuras alterações, reduzindo a possibilidade de
erros e facilitando a evolução do sistema

Essa arquitetura foi definida para oferecer uma estrutura organizada, confiável e preparada para a evolução do sistema.

### PROTOTIPAGEM DE INTERFACE (WIREFRAMES)

<img width="511" height="398" alt="image" src="https://github.com/user-attachments/assets/0ef78a47-f78c-43ee-946a-cc7b7c9878c0" />

Legenda: Tela de login, local para fazer a entrada no site como funcionário e cliente.

<img width="809" height="510" alt="image" src="https://github.com/user-attachments/assets/8defc9d2-3e6b-455e-bfbb-a08c41d1cd6b" />

Legenda: Tela de carros, mostra os carros cadastrados no sistema e também pode aplicar o filtro de disponibilidade e indisponibilidade.

<img width="846" height="505" alt="image" src="https://github.com/user-attachments/assets/4a72e961-25a2-4167-9f30-0aa9faa690a0" />

Legenda:Tela de cadastro/edição de carro, permite criar e editar carros.

<img width="724" height="500" alt="image" src="https://github.com/user-attachments/assets/4300ebbc-2a19-4a1a-910f-c4396ba0c26b" />
Legenda: Tela de clientes, cadastro, edição e busca de clientes.

<img width="780" height="481" alt="image" src="https://github.com/user-attachments/assets/fc5a8cc1-21cb-4421-8ecb-c0b4cb2f3cab" />

Legenda: Tela do aluguel, permite realizar o aluguel.

<img width="762" height="481" alt="image" src="https://github.com/user-attachments/assets/0989e121-78cf-4903-94e1-f83dd8686a85" />

Legenda: Tela de controle dos aluguéis, mostra os aluguéis ativos, permite registrar a devolução do veículo e consultar o histórico de aluguéis.

<img width="409" height="539" alt="image" src="https://github.com/user-attachments/assets/5013ff1e-1284-4c6f-9eee-5b9cee86ce48" />

Legenda: Tela de controle dos aluguéis, mostra os aluguéis ativos, permite registrar a devolução do veículo e consultar o histórico de aluguéis.










