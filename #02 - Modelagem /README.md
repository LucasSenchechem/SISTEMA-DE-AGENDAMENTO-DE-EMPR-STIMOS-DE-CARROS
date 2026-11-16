# Modelagem

A modelagem do sistema foi desenvolvida para representar as principais funcionalidades, os usuários envolvidos e a estrutura das classes responsáveis pelo gerenciamento de veículos, clientes e aluguéis.

Foram utilizados diagramas UML (Linguagem de Modelagem Unificada) para facilitar a compreensão da organização e do funcionamento do sistema.

## Diagrama de Caso e Uso:
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/6982e174-037e-43dd-90ca-bb4b156f8ffc" />

O diagrama de casos de uso apresenta as principais funcionalidades disponíveis para os dois atores do sistema:

Cliente: consultar veículos disponíveis e realizar aluguéis.

Funcionário: cadastrar, consultar, atualizar e remover veículos e clientes, realizar aluguéis, registrar devoluções, consultar históricos e gerar relatórios.

Esse diagrama permite visualizar como cada usuário interage com o sistema.


## Diagrama de classes
<img width="2309" height="1817" alt="Diagrama em branco" src="https://github.com/user-attachments/assets/ad431729-b4c7-4c87-b890-2a3978eb87b8" />

O diagrama de classes representa a estrutura do sistema, incluindo suas principais entidades:

Veículo: armazena as informações e a situação de disponibilidade dos carros.

Cliente: representa os usuários cadastrados para realizar aluguéis.

Funcionário: representa os responsáveis pelas operações administrativas.

Aluguel: registra a relação entre cliente e veículo, incluindo as informações da locação.

O modelo também contempla classes de gerenciamento, responsáveis por organizar as operações relacionadas a cada entidade.

## Regra de Negócio
A modelagem considera regras importantes para garantir a consistência das informações, como:

Um veículo não pode possuir dois aluguéis ativos simultaneamente.

Apenas veículos disponíveis podem ser alugados.

Cada veículo deve possuir uma placa única.

Cada cliente deve possuir um CPF único.

Após a devolução, o veículo volta a ficar disponível, desde que não necessite de manutenção.

Os aluguéis encerrados permanecem registrados no histórico.

Esses modelos servem como referência para o desenvolvimento, a implementação das funcionalidades e a realização dos testes do sistema.


