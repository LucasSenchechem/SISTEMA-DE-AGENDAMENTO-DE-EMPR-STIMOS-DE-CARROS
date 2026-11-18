# Modelagem

A modelagem do sistema foi desenvolvida para representar as principais funcionalidades, os usuários envolvidos e a estrutura das classes responsáveis pelo gerenciamento de veículos, clientes e aluguéis.

Foram utilizados diagramas UML (Linguagem de Modelagem Unificada) para facilitar a compreensão da organização e do funcionamento do sistema.

### Diagrama de Caso e Uso:
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/6982e174-037e-43dd-90ca-bb4b156f8ffc" />

O diagrama de casos de uso apresenta as principais funcionalidades disponíveis para os dois atores do sistema:

Cliente: consultar veículos disponíveis e realizar aluguéis.

Funcionário: cadastrar, consultar, atualizar e remover veículos e clientes, realizar aluguéis, registrar devoluções, consultar históricos e gerar relatórios.

Esse diagrama permite visualizar como cada usuário interage com o sistema.


### Diagrama de classes
<img width="2309" height="1817" alt="Diagrama em branco" src="https://github.com/user-attachments/assets/ad431729-b4c7-4c87-b890-2a3978eb87b8" />

O diagrama de classes representa a estrutura do sistema, incluindo suas principais entidades:

Veículo: armazena as informações e a situação de disponibilidade dos carros.

Cliente: representa os usuários cadastrados para realizar aluguéis.

Funcionário: representa os responsáveis pelas operações administrativas.

Aluguel: registra a relação entre cliente e veículo, incluindo as informações da locação.

O modelo também contempla classes de gerenciamento, responsáveis por organizar as operações relacionadas a cada entidade.

### Mapeamento dos requisitos nos diagramas 
O mapeamento dos requisitos e das regras de negócio nos modelos permite relacionar as funcionalidades e condições definidas anteriormente com os elementos apresentados nos diagramas de casos de uso e de classes. 
Dessa forma, é possível verificar como as necessidades identificadas no sistema estão representadas na sua modelagem.
Mapeamento dos Requisitos Funcionais:
No diagrama de casos de uso, os requisitos funcionais foram representados por meio das principais ações disponíveis para os usuários:

Carros (RF01 a RF09): representados pelas funcionalidades de cadastrar, consultar, buscar, atualizar e remover veículos, além da consulta de carros disponíveis.
Clientes (RF10 a RF15): representados pelas funcionalidades de cadastrar, consultar, buscar, atualizar e remover clientes.
Aluguéis (RF16 a RF20): representados pelas funcionalidades de realizar aluguel, registrar devolução, listar aluguéis ativos, consultar histórico e gerar relatórios.

No diagrama de classes, esses requisitos estão relacionados às entidades Veículo, Cliente, Funcionário e Aluguel, além das classes responsáveis pelo gerenciamento de cada uma dessas partes do sistema.
Mapeamento das Regras de Negócio:
As regras de negócio estão relacionadas aos elementos do diagrama de classes, principalmente às informações e aos relacionamentos entre as entidades.
RN01 e RN02: relacionadas à classe Veículo, que possui identificação e placa para o controle dos veículos cadastrados.
RN03, RN04 e RN11: relacionadas à classe Veículo e ao seu status, que permite identificar sua disponibilidade para aluguel. Entretanto, a condição específica de manutenção ainda não está representada no diagrama.
RN05 e RN06: relacionadas à classe Cliente, que armazena as informações cadastrais, incluindo o CPF.
RN07: representada pelo relacionamento entre as classes Aluguel, Cliente e Veículo.
RN08 e RN09: relacionadas à alteração do status do veículo durante o processo de aluguel e devolução.
RN10: representada pelos atributos de data de retirada e data de devolução presentes na classe Aluguel.
RN12: relacionada à funcionalidade de consulta do histórico de aluguéis, apresentada no diagrama de casos de uso.



