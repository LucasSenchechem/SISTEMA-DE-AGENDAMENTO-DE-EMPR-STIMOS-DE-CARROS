# Manutenção

## Objetivo

Esta seção apresenta o planejamento de manutenção e evolução do Sistema de Agendamento de Empréstimos de Carros, visando garantir sua confiabilidade, segurança e facilidade de atualização.

## Tipos de manutenção previstos

Foram planejadas quatro possibilidades de manutenção:

### Corretiva: 
corrigir possíveis falhas na validação de placas dos veículos.

### Adaptativa:
permitir a migração do banco de dados para outro SGBD ou ambiente de hospedagem.

### Perfectiva: 
adicionar alertas para aluguéis com devolução atrasada.

### Preventiva: 
separar a geração de relatórios em um componente próprio, melhorando a organização do código.

## Análise de impacto

Antes de implementar qualquer alteração, deverão ser identificados os componentes afetados, os requisitos relacionados e os testes necessários.

As mudanças poderão afetar principalmente as classes GerenciaVeiculo e GerenciaAluguel, a camada de persistência e a interface dos funcionários.

## Gerenciamento de riscos

### Os principais riscos identificados são:

- Aluguel simultâneo do mesmo veículo para clientes diferentes.
- Perda ou inconsistência de informações.
- Acesso não autorizado aos dados.
- Falhas de validação.
- Atrasos no desenvolvimento.
- Alterações ou inconsistências nos requisitos.

Para reduzir esses riscos, estão previstos testes, validações, controle de acesso, backups e revisões periódicas.

## Controle de alterações

As mudanças deverão ser registradas e avaliadas antes da implementação. Após cada alteração, os requisitos, diagramas e casos de teste relacionados deverão ser atualizados.

O acompanhamento será realizado ao final de cada incremento de duas semanas, conforme o planejamento do projeto.

## Situação do projeto

As manutenções apresentadas são propostas para a evolução futura do sistema, não funcionalidades já implementadas.
