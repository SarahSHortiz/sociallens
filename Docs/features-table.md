# 📊 TABELA DE FUNCIONALIDADES

# Documentação de Casos de Uso (Modelo do Usuário)

Esta é a documentação dos Casos de Uso no formato solicitado, convertida a partir do texto fornecido.

---

## UC01 – Abrir Conta

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC01 – Abrir Conta |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que um Usuário se cadastre na plataforma com dados básicos e receba credenciais de acesso. |
| **Pré-condição** | O usuário não possui conta cadastrada na plataforma. |
| **Pós-Condição** | Usuário cadastrado e autenticado, podendo acessar funcionalidades permitidas pelo seu perfil. |
| **Requisitos Funcionais** | RF09 |
| **Requisitos Não Funcionais** | RNF01, RNF03 |
| **Tela Envolvida** | Tela de Cadastro |
| **Trativa de Erros** | Senha deve ter no mínimo 8 caracteres, conter letras maiúsculas, minúsculas e números. Apenas e-mails corporativos podem ser cadastrados. |
| **Restrições / Validações** | Senha deve ter no mínimo 8 caracteres, conter letras maiúsculas, minúsculas e números. Apenas e-mails corporativos podem ser cadastrados. |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a tela de cadastro | 02 - Sistema exibe formulário de cadastro |
| 03 – O usuário preenche os dados: Email, senha, empresa. | 04 - Sistema valida campos obrigatórios e formato do e-mail. |
| 05 – Usuário envia formulário | 06 – Sistema verifica se e-mail já está cadastrado |
| 07 – Usuário aguarda a confirmação | 08 – Sistema cria registro da senha e salva no banco |
| 09 - Usuário recebe a mensagem de sucesso | |

**Cenário Alternativo I - Email já cadastrado**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema detecta email existente |
| | Sistema exibe a mensagem de email já cadastrado |

**Cenário Alternativo II - Campos obrigatórios não preenchidos**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema identifica campos não preenchidos |
| | Sistema exibe mensagem de erro, destacando os campos obrigatórios a serem preenchidos |

**Cenário Alternativo III - Senha não atende critérios de segurança**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema valida senha |
| | Sistema exibe mensagem de erro e reforça que a senha não atende os requisitos |

---

## UC02 – Login

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC02 – Login |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário realize o login na plataforma com dados básicos e receba credenciais de acesso. |
| **Pré-condição** | O usuário não efetuou o login na plataforma e está cadastrado e autenticado anteriormente. |
| **Pós-Condição** | Usuário logado podendo acessar funcionalidades permitidas pelo seu perfil. |
| **Requisitos Funcionais** | RF09 |
| **Requisitos Não Funcionais** | RNF01 (Responsividade), RNF03 (Armazenamento Seguro), RNF04 (Confiabilidade), RNF06 (Histórico) |
| **Tela Envolvida** | Tela de Login |
| **Trativa de Erros** | O sistema deve bloquear o login por 2 minutos, após 5 tentativas de login inválidas. |
| **Restrições / Validações** | Senha deve ter no mínimo 8 caracteres, conter letras maiúsculas, minúsculas e números. Apenas e-mails corporativos que já foram cadastrados. |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a tela de login | 02 - Sistema exibe formulário de login |
| 03 – O usuário preenche os dados: Email, senha. | 04 - Sistema valida campos obrigatórios e formato do e-mail. |
| 05 – Usuário envia formulário | 06 – Sistema verifica se e-mail já está cadastrado |
| 07 – Usuário aguarda a confirmação | 08 – Sistema cria registro da senha e salva no banco |
| 09 - Usuário recebe a mensagem de sucesso | |

**Cenário Alternativo I - Email não cadastrado**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema detecta email existente |
| | Sistema exibe a mensagem "E-mail ou senha incorretos". (Contador de tentativas é incrementado). |

**Cenário Alternativo II - Campos obrigatórios não preenchidos**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema identifica campos não preenchidos |
| | Sistema exibe mensagem de erro, destacando os campos obrigatórios a serem preenchidos |

**Cenário Alternativo III - Senha/email Incorreto**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema valida senha |
| | Sistema exibe mensagem de erro e reforça que a senha/email não atende os requisitos |

---

## UC03 – Recuperar Senha

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC03 – Recuperar Senha |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário recupere sua senha. |
| **Pré-condição** | O usuário perdeu a senha. |
| **Pós-Condição** | O usuário passa a ter acesso ao sistema devido à recuperação da senha. |
| **Requisitos Funcionais** | RF09 |
| **Requisitos Não Funcionais** | RNF01 (Responsividade), RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Recuperação de Senha |
| **Trativa de Erros** | O link de recuperação de senha deve expirar em 30 minutos. |
| **Restrições / Validações** | Senha deve ter no mínimo 8 caracteres, conter letras maiúsculas, minúsculas e números. Apenas e-mails corporativos podem ser cadastrados. |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a tela de recuperação de senha e informa seu e-mail. | 02 - Sistema valida o formato do e-mail. |
| 03 – Usuário envia a solicitação. | 04 – Sistema verifica se o e-mail está cadastrado. |
| 05 – Usuário verifica sua caixa de entrada. | 06 – Sistema gera um token de recuperação e envia um e-mail com o link de redefinição. |
| 07 – Usuário clica no link e insere a nova senha. | 08 – Sistema valida a nova senha (critérios de segurança) e o token. |
| 09 – Usuário recebe a mensagem de sucesso. | 10 – Sistema atualiza a senha no banco de dados. |

**Cenário Alternativo I - E-mail não cadastrado**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema detecta e-mail não cadastrado e exibe a mensagem "Se o e-mail estiver cadastrado, você receberá um link de redefinição". |

**Cenário Alternativo II - Link Expirado**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema detecta que o token de recuperação expirou. |
| | Sistema exibe a mensagem "Link expirado. Por favor, solicite uma nova recuperação de senha." |

---

## UC04 – Escolher/Atualizar Plano

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC04 – Escolher/Atualizar Plano |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário selecione ou modifique seu plano de serviço, habilitando o acesso às funcionalidades e dados correspondentes. |
| **Pré-condição** | Usuário autenticado. |
| **Pós-Condição** | Plano do usuário atualizado e ativo no sistema. |
| **Requisitos Funcionais** | RF09 (Controle de Acesso) |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Planos e Pagamento |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a tela de Planos (ou é redirecionado pelo UC02). | 02 - Sistema exibe os planos disponíveis com suas funcionalidades e preços. |
| 03 – O usuário seleciona um plano. | 04 - Sistema exibe o resumo da transação. |
| 05 – Usuário confirma e insere os dados de pagamento. | 06 – Sistema processa o pagamento via gateway externo. |
| 05 – Usuário confirma e insere os dados de pagamento. | 08 – Sistema recebe a confirmação de pagamento e ativa o plano. |
| 09 – Usuário recebe a mensagem de sucesso e é direcionado para o Dashboard. | |

**Cenário Alternativo I - Falha no Pagamento**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema recebe notificação de falha do gateway de pagamento. |
| | Sistema exibe a mensagem "Falha na transação. Por favor, tente novamente ou use outro método de pagamento." |

---

## UC05 – Visualizar Dashboards

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC05 – Visualizar Dashboards |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário visualize os principais indicadores e gráficos de performance da sua empresa e concorrentes. |
| **Pré-condição** | Usuário autenticado e com plano ativo. |
| **Pós-Condição** | O usuário visualiza os dados atualizados. |
| **Requisitos Funcionais** | RF02 (Exibir dashboards com gráficos), RF07 (Comparar desempenho entre unidades), RF08 (Atualizar dashboards dinamicamente), RF10 (Exibir métricas de volume e tendência). |
| **Requisitos Não Funcionais** | RNF01 (Responsividade), RNF02 (Tempo de Resposta), RNF04 (Confiabilidade), RNF05 (Usabilidade), RNF07 (Escalabilidade) |
| **Tela Envolvida** | Tela de Dashboards |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a funcionalidade de Dashboards. | 02 - Sistema carrega e exibe os dashboards padrão. |
| 03 – O usuário interage com os gráficos. | 04 - Sistema atualiza as visualizações conforme a interação. |

---

## UC06 – Gerar Relatórios

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC06 – Gerar Relatórios |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário gere relatórios detalhados dos dados analisados em formatos para download. |
| **Pré-condição** | Usuário autenticado e com plano ativo. |
| **Pós-Condição** | O usuário recebe o arquivo de relatório solicitado. |
| **Requisitos Funcionais** | RF04 (Gerar relatórios exportáveis), RF08 (Atualizar relatórios dinamicamente) |
| **Requisitos Não Funcionais** | RNF02 (Tempo de Resposta), RNF05 (Usabilidade) |
| **Tela Envolvida** | Tela de Gerar Relatórios |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a funcionalidade de Relatórios. | 02 - Sistema exibe as opções de relatório e filtros disponíveis. |
| 03 – O usuário seleciona o tipo de relatório, período e formato. | 04 - Sistema processa a solicitação e gera o arquivo. |
| 05 – O usuário clica no botão de download. | 06 – Sistema disponibiliza o arquivo para download. |

---

## UC07 – Visualizar Notificações

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC07 – Visualizar Notificações |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário visualize alertas e avisos importantes gerados pelo sistema. |
| **Pré-condição** | Usuário autenticado. |
| **Pós-Condição** | As notificações são exibidas e marcadas como lidas. |
| **Requisitos Funcionais** | RF05 (Criar alertas automáticos). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Notificações |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário clica no ícone de notificações. | 02 - Sistema exibe a lista de notificações pendentes. |
| 03 – O usuário clica em uma notificação. | 04 - Sistema exibe o detalhe da notificação e a marca como lida. |

---

## UC08 – Personalizar Filtros

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC08 – Personalizar Filtros |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário crie e salve conjuntos de filtros personalizados para uso posterior. |
| **Pré-condição** | Usuário autenticado. |
| **Pós-Condição** | O novo conjunto de filtros é salvo e disponível para uso. |
| **Requisitos Funcionais** | RF03 (Permitir filtragem por unidade, período e palavra-chave). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Filtros |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a tela de gerenciamento de filtros. | 02 - Sistema exibe a lista de filtros salvos e a opção para criar um novo. |
| 03 – O usuário define os critérios do novo filtro (ex: período, localização, palavras-chave). | 04 - Sistema valida os critérios. |
| 05 – O usuário salva o filtro. | 06 – Sistema armazena o filtro personalizado. |

---

## UC09 – Adicionar Concorrente

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC09 – Adicionar Concorrente |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário adicione uma nova empresa concorrente para monitoramento e análise. |
| **Pré-condição** | Usuário autenticado e com plano ativo que permita a adição de concorrentes. |
| **Pós-Condição** | O concorrente é adicionado à lista de monitoramento e o sistema inicia a coleta de dados. |
| **Requisitos Funcionais** | RF01 (Importar e armazenar avaliações), RF09 (Controle de Acesso). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Adicionar Concorrentes |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a tela de gerenciamento de concorrentes. | 02 - Sistema exibe a lista atual de concorrentes e o limite do plano. |
| 03 – O usuário insere os dados do novo concorrente (ex: nome, redes sociais, endereço). | 04 - Sistema verifica se o limite de concorrentes do plano foi atingido. |
| 05 – O usuário confirma a adição. | 06 – Sistema valida os dados e registra o novo concorrente. |
| 07 – Usuário recebe a mensagem de sucesso. | 08 – Sistema inicia a coleta de dados para o novo concorrente. |

**Cenário Alternativo I - Limite de Concorrentes Atingido**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| | Sistema detecta que o limite do plano foi atingido. |
| | Sistema exibe a mensagem "Limite de concorrentes atingido. Por favor, atualize seu plano para adicionar mais." |

---

## UC10 – Ver Análise Competitiva

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC10 – Ver Análise Competitiva |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário visualize relatórios e dashboards específicos que comparam a performance de sua empresa com a dos concorrentes monitorados. |
| **Pré-condição** | Usuário autenticado, com plano ativo que inclua a funcionalidade de Análise Competitiva e pelo menos um concorrente adicionado. |
| **Pós-Condição** | O usuário visualiza a análise comparativa. |
| **Requisitos Funcionais** | RF07 (Comparar desempenho entre unidades). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Análise Competitiva |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário acessa a funcionalidade de Análise Competitiva. | 02 - Sistema carrega os dados comparativos entre a empresa do usuário e os concorrentes. |
| 03 – O usuário seleciona o tipo de comparação (ex: por métrica, por período). | 04 - Sistema exibe os dashboards e relatórios de análise competitiva. |

---

## UC11 – Filtrar Redes Sociais

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC11 – Filtrar Redes Sociais |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário refine a visualização de dados e relatórios aplicando filtros específicos para redes sociais. |
| **Pré-condição** | Usuário dentro de um caso de uso base (UC05 ou UC06). |
| **Pós-Condição** | Os dados exibidos no caso de uso base são atualizados conforme o filtro. |
| **Requisitos Funcionais** | RF03 (Permitir filtragem por palavra-chave). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Filtro de Redes Sociais |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário clica no botão "Filtrar por Redes Sociais" (dentro do UC base). | 02 - Sistema exibe as opções de redes sociais disponíveis para filtro. |
| 03 – O usuário seleciona as redes sociais desejadas. | 04 - Sistema aplica o filtro aos dados do UC base. |
| 05 – O usuário recebe a confirmação da aplicação do filtro. | 06 – Sistema retorna o controle ao UC base com os dados filtrados. |

---

## UC12 – Filtrar Google Maps

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC12 – Filtrar Google Maps |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Usuário |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o usuário refine a visualização de dados e relatórios aplicando filtros de localização geográfica. |
| **Pré-condição** | Usuário dentro de um caso de uso base (UC05 ou UC06). |
| **Pós-Condição** | Os dados exibidos no caso de uso base são atualizados conforme o filtro. |
| **Requisitos Funcionais** | RF03 (Permitir filtragem por unidade, período e palavra-chave). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Filtro de Google Maps |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O usuário clica no botão "Filtrar por Localização" (dentro do UC base). | 02 - Sistema exibe o mapa ou formulário para definição da área de filtro. |
| 03 – O usuário define os limites geográficos do filtro. | 04 - Sistema aplica o filtro aos dados do UC base. |
| 05 – O usuário recebe a confirmação da aplicação do filtro. | 06 – Sistema retorna o controle ao UC base com os dados filtrados. |

---

## UC13 – Gerenciar Usuários

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC13 – Gerenciar Usuários |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Administrador |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o Administrador execute operações CRUD (Criar, Ler, Atualizar, Deletar) sobre as contas dos usuários do sistema. |
| **Pré-condição** | Administrador autenticado. |
| **Pós-Condição** | O registro de usuários é atualizado. |
| **Requisitos Funcionais** | RF09 (Controle de Acesso). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Gerenciamento de Usuários |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O Administrador acessa a tela de Gerenciamento de Usuários. | 02 - Sistema exibe a lista de todos os usuários. |
| 03 – O Administrador seleciona um usuário e escolhe uma ação (ex: Editar, Suspender). | 04 - Sistema executa a ação solicitada. |
| 05 – O Administrador recebe a confirmação da operação. | 06 – Sistema atualiza o registro do usuário. |

---

## UC14 – Gerenciar Organizações

| Campo | Detalhe |
| :--- | :--- |
| **Nome do Caso de Uso** | UC14 – Gerenciar Organizações |
| **Classificação** | Caso de Uso Geral |
| **Controle de Versão** | 1.0.0 – 20/10/2025 – Resp: Sarah Hortiz |
| **Ator Principal** | Administrador |
| **Ator Secundário** | Sistema |
| **Resumo** | Permite que o Administrador execute operações CRUD sobre as organizações (empresas) cadastradas no sistema. |
| **Pré-condição** | Administrador autenticado. |
| **Pós-Condição** | O registro de organizações é atualizado. |
| **Requisitos Funcionais** | RF09 (Controle de Acesso). |
| **Requisitos Não Funcionais** | RNF03 (Armazenamento Seguro) |
| **Tela Envolvida** | Tela de Gerenciamento de Organizações |
| **Trativa de Erros** | *** |
| **Restrições / Validações** | *** |

**Cenário Principal**

| Ações dos Atores | Ações do Sistema |
| :--- | :--- |
| 01 - O Administrador acessa a tela de Gerenciamento de Organizações. | 02 - Sistema exibe a lista de todas as organizações. |
| 03 – O Administrador seleciona uma organização e escolhe uma ação (ex: Editar Plano, Adicionar Usuário). | 04 - Sistema executa a ação solicitada. |
| 05 – O Administrador recebe a confirmação da operação. | 06 – Sistema atualiza o registro da organização. |
