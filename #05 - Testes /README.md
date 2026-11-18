# Testes
Os casos de teste têm como objetivo verificar se as funcionalidades do sistema apresentam os resultados esperados e respeitam os requisitos e as regras de negócio estabelecidos anteriormente. Para isso, foram definidos cenários que representam situações comuns de utilização, além de situações inválidas que deverão ser tratadas pelo sistema. Cada caso de teste apresenta uma condição inicial, uma ação realizada pelo usuário e o resultado esperado.
### CT01:  Cadastro de veículo
- Requisitos relacionados: RF01, RN01 e RN02.
- Condição inicial: Funcionário autenticado no sistema.
- Procedimento: Cadastrar um veículo com dados válidos e placa ainda não registrada.
- Resultado esperado: O veículo deverá ser cadastrado com sucesso, recebendo um identificador único e ficando disponível para consulta.
  
### CT02:  Cadastro de veículo com placa duplicada
- Requisitos relacionados: RF01, RN02 e RNF06.
- Condição inicial: Existência de um veículo previamente cadastrado.
- Procedimento: Tentar cadastrar outro veículo utilizando a mesma placa.
- Resultado esperado: O sistema deverá impedir o cadastro e informar que a placa já está registrada.
  
### CT03:  Cadastro de cliente com CPF duplicado
- Requisitos relacionados: RF10, RN06 e RNF06.
- Condição inicial: Existência de um cliente previamente cadastrado.
- Procedimento: Tentar cadastrar outro cliente utilizando o mesmo CPF.
- Resultado esperado: O sistema deverá recusar o cadastro duplicado e apresentar uma mensagem informando a inconsistência.
  
### CT04:  Realização de aluguel válido
- Requisitos relacionados: RF16, RN03, RN05, RN07, RN08 e RN10.
- Condição inicial: Cliente cadastrado e veículo disponível.
- Procedimento: Selecionar o veículo e confirmar a realização do aluguel.
- Resultado esperado: O aluguel deverá ser registrado, associado ao cliente e ao veículo, com a data de início armazenada. O status do veículo deverá ser atualizado para indisponível.
  
### CT05: Tentativa de aluguel de veículo indisponível
- Requisitos relacionados: RF16, RN03, RN04 e RNF04.
- Condição inicial: Veículo vinculado a um aluguel ativo.
- Procedimento: Tentar realizar outro aluguel utilizando o mesmo veículo.
- Resultado esperado: O sistema deverá bloquear a operação e informar que o veículo não está disponível, evitando a existência de dois aluguéis ativos simultâneos.
  
### CT06:  Tentativa de aluguel de veículo em manutenção
- Requisitos relacionados: RF16 e RN11.
- Condição inicial: Veículo identificado como indisponível por necessidade de manutenção.
- Procedimento: Tentar realizar um aluguel desse veículo.
- Resultado esperado: O sistema deverá impedir a operação enquanto existir o impedimento.
  
### CT07:  Registro de devolução
- Requisitos relacionados: RF17, RN09, RN10 e RN12.
- Condição inicial: Existência de um aluguel ativo.
- Procedimento: Registrar a devolução de um veículo que não necessita de manutenção.
- Resultado esperado: O aluguel deverá ser encerrado, a data de devolução deverá ser registrada e o veículo deverá voltar a ficar disponível. O registro deverá permanecer no histórico de aluguéis.
  
### CT08: Controle de acesso
- Requisitos relacionados: RNF05.
- Condição inicial: Usuário sem autenticação de funcionário.
- Procedimento: Tentar acessar uma funcionalidade administrativa, como o cadastro ou a remoção de veículos.
- Resultado esperado: O sistema deverá bloquear a operação, permitindo sua execução somente por funcionários autorizados.
  
### CT09:  Persistência das informações
- Requisitos relacionados: RNF07.
- Condição inicial: Existência de veículos, clientes e aluguéis cadastrados.
- Procedimento: Encerrar a aplicação, acessá-la novamente e consultar os registros anteriores.
- Resultado esperado: As informações deverão permanecer armazenadas e disponíveis para consulta.
  
### CT10:  Desempenho das consultas
- Requisitos relacionados: RF05, RF06, RF13 e RNF02.
- Condição inicial: Sistema com registros cadastrados.
- Procedimento: Realizar buscas de veículos por ID e placa e de clientes por CPF, medindo o tempo de resposta.
- Resultado esperado: Cada consulta deverá apresentar seu resultado em até 3 segundos.

### CT11: Listagens de veículos e estoque

- Requisitos relacionados: RF02, RF03, RF04 e RF07
- Condição inicial: veículos disponíveis e indisponíveis cadastrados
- Procedimento: consultar todos os veículos, apenas os disponíveis, apenas os indisponíveis e o estoque 
- Resultado esperado: Cada consulta retorna somente os veículos correspondentes, e o estoque apresenta a divisão entre disponíveis e indisponíveis

### CT12: Atualização de dados 
- Requisitos relacionados: RF08, RF14, RN02, RN06 
- Condição inicial: dados de clientes e veículos cadastrados no sistema
- Procedimento: alterar dados de um veículo e de um cliente; tentar trocar a placa e o CPF por valores já cadastrados  
- Resultado esperado: alterações válidas são gravadas; duplicidades são recusadas com mensagem

### CT13: Remoção de registros 
- Requisitos relacionados: RF09, RF15, RN12 
- Condição inicial: veículo e cliente cadastrado no sistema
- Procedimento: remover um veículo e um cliente sem aluguéis; tentar remover um veículo com aluguel ativo 
- Resultado esperado: os registros sem aluguéis deixam de aparecer nas consultas; a remoção de veículo com aluguel ativo é bloqueada; o histórico de aluguéis não é apagado

### CT14: Consultas de clientes e aluguéis 
- Requisitos relacionados: RF11, RF12, RF18, RF19, RN12 
- Condição inicial: clientes cadastrados e aluguéis ativos
- Procedimento: listar clientes, buscar um cliente por ID, listar aluguéis ativos e consultar o histórico 
- Resultado esperado: os dados correspondem aos cadastrados; a lista de ativos contém só aluguéis não encerrados; o histórico traz os encerrados
 
### CT15: Geração de relatório  
- Requisitos relacionados: RF20, RNF05 
- Condição inicial: funcionário cadastrado
- Procedimento: com funcionário autenticado, gerar o relatório; tentar gerar sem autenticação 
- Resultado esperado: o relatório é gerado com dados de aluguéis e veículos e com CPF mascarado; usuário sem autenticação de funcionário é bloqueado

### CT16: Acesso por navegadores e dispositivos 
- Requisitos relacionados: RNF03, RNF08 
- Condição inicial: carros cadastrados e disponíveis para aluguel
- Procedimento: acessar o sistema pela internet em computador e celular, nos navegadores mais comuns, consultando carros e realizando um aluguel 
- Resultado esperado: o sistema abre e funciona nos navegadores testados, sem necessidade de ir à locadora 


Os casos de teste apresentados serão utilizados durante as etapas de verificação do sistema, conforme o processo incremental definido no capítulo 5. A execução dos testes permitirá identificar possíveis falhas, corrigir inconsistências e avaliar se os requisitos estabelecidos foram atendidos.

Os resultados descritos representam os comportamentos esperados do sistema, não constituindo evidência de testes já executados.
