
### Requisitos Funcionais
|Id|Descrição|
|---|---|
|RF01|O sistema deve permitir o cadastro de usuários com nome, e-mail e senha.|
|RF02|O sistema deve permitir que usuários realizem login utilizando e-mail e senha.|
|RF03|O sistema deve permitir a criação, edição e exclusão de cursos por administradores.|
|RF04|O sistema deve permitir que usuários se matriculem em cursos disponíveis.|
|RF05|O sistema deve gerar relatórios de desempenho dos usuários nos cursos.|

### Requisitos Não Funcionais
|Id|Descrição|
|---|---|
|RNF01|O sistema deve garantir um tempo de resposta inferior a 2 segundos para qualquer requisição.|
|RNF02|O sistema deve estar disponível pelo menos 99,5% do tempo mensal.|
|RNF03|O sistema deve armazenar as senhas de forma segura utilizando hashing e salting.|
|RNF04|O sistema deve ser compatível com os navegadores Chrome, Firefox e Edge nas versões mais recentes.|
|RNF05|O sistema deve suportar pelo menos 500 usuários simultâneos sem degradação perceptível do desempenho.|

### Relação entre Requisitos Funcionais e Não Funcionais
|Id|Descrição|
|---|---|
|RF01|RNF03 (armazenamento seguro de senhas), RNF04 (compatibilidade com navegadores)|
|RF02|RNF01 (tempo de resposta rápido), RNF03 (armazenamento seguro de senhas)|
|RF03|RNF05 (suporte a múltiplos usuários), RNF01 (tempo de resposta rápido)|
|RF04|RNF05 (suporte a múltiplos usuários), RNF04 (compatibilidade com navegadores)|
|RF05|RNF01 (tempo de resposta rápido), RNF02 (disponibilidade do sistema)|
