# Verificação e validação
A verificação e a validação são processos fundamentais para garantir a qualidade do Sistema de Agendamento de Empréstimos de Carros. Embora estejam relacionadas, possuem objetivos diferentes. A verificação busca identificar se o sistema está sendo desenvolvido corretamente, de acordo com os requisitos e especificações estabelecidas. Já a validação procura confirmar se o sistema atende às necessidades reais dos usuários e cumpre os objetivos para os quais foi proposto.

Verificação: No projeto, a verificação será realizada por meio da análise dos requisitos funcionais e não funcionais, das regras de negócio, dos diagramas e da execução dos casos de teste apresentados na seção 6.2.
Por exemplo, o caso de teste CT05 verificará se o sistema impede que um veículo já alugado seja vinculado a outro aluguel ativo, conforme a regra de negócio RN04. Da mesma forma, o CT03 verificará se o sistema bloqueia o cadastro de clientes com CPF duplicado, respeitando a RN06.
Também serão verificados aspectos como o tempo de resposta das consultas, a segurança de acesso e a persistência das informações, conforme os requisitos não funcionais definidos na seção 2.3.

Validação: A validação terá como objetivo avaliar se as funcionalidades propostas realmente atendem às necessidades dos clientes e funcionários da locadora.
Esse processo será realizado por meio da apresentação dos incrementos do sistema aos stakeholders, conforme a abordagem incremental e iterativa definida no capítulo 5.
Por exemplo, os funcionários poderão avaliar se o processo de cadastro e devolução de veículos é simples e adequado à rotina da locadora. Já os clientes poderão avaliar se a consulta de veículos disponíveis e a realização de aluguéis são práticas e intuitivas.
As avaliações permitirão identificar possíveis dificuldades de utilização e necessidades de melhoria, mesmo quando as funcionalidades estiverem de acordo com os requisitos técnicos.

Diferença entre os processos: Enquanto a verificação procura responder à pergunta "Estamos construindo o sistema corretamente?", a validação busca responder "Estamos construindo o sistema certo?".
Dessa forma, ambos os processos serão aplicados ao longo dos ciclos de desenvolvimento. A verificação contribuirá para identificar falhas e inconsistências técnicas, enquanto a validação permitirá avaliar a adequação do sistema às expectativas dos usuários.
A utilização conjunta desses processos contribuirá para o desenvolvimento de uma solução confiável, funcional e alinhada às necessidades da locadora e de seus clientes.
