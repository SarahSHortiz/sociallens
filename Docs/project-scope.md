| **ID** | **Tipo**         | **Descrição**                                                                                                                                                                          |
| :----- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RN01   | Regra de Negócio | A plataforma só analisará dados públicos do Google Maps.                                                                                                                               |
| RN02   | Regra de Negócio | Cada usuário terá acesso apenas às informações da sua empresa.                                                                                                                         |
| RN03   | Regra de Negócio | Avaliações devem ser coletadas automaticamente e armazenadas com histórico.                                                                                                            |
| RN04   | Regra de Negócio | Apenas usuários autorizados podem gerar relatórios e alertas.                                                                                                                          |
| RN05   | Regra de Negócio | Alertas devem identificar problemas recorrentes, como filas ou demora no atendimento.                                                                                                  |
| RN06   | Regra de Negócio | Cada unidade/loja terá um identificador único dentro da organização.                                                                                                                   |
| RNF01  | Não Funcional    | Responsividade e Acessibilidade: Plataforma deve ser exibida corretamente em telas de ≥ 360x640 (mobile) e ≥ 1366x768 (desktop).                                                       |
| RNF02  | Não Funcional    | Tempo de Resposta: Todas as requisições devem responder em ≤ 2 minutos para até 500 avaliações simultâneas por usuário.                                                                |
| RNF03  | Não Funcional    | Armazenamento Seguro: Senhas devem ser armazenadas com hash seguro. Todos os dados sensíveis devem ser transmitidos via HTTPS, e backups diários devem ter retenção mínima de 30 dias. |
| RNF04  | Não Funcional    | Confiabilidade / Multiusuário: Sistema deve suportar ≥ 10 usuários simultâneos sem degradação de performance.                                                                          |
| RNF05  | Não Funcional    | Usabilidade / Interface Intuitiva: Usuário deve conseguir gerar relatório ou alerta em ≤ 5 cliques; dashboards devem ter ≥ 95% de legibilidade.                                        |
| RNF06  | Não Funcional    | Histórico: Todas as ações de usuários devem ser registradas com timestamp, usuário responsável e tipo de ação.                                                                         |
| RNF07  | Não Funcional    | Escalabilidade: Sistema deve suportar até 500 avaliações por empresa sem degradação de performance.                                                                                    |


| **ID** | **Descrição**                                                                                       | **Casos de Uso Relacionados (UCs)**     |
| :----- | :-------------------------------------------------------------------------------------------------- | :-------------------------------------- |
| RF01   | Importar e armazenar avaliações do Google Maps automaticamente.                                     | UC09, UC15                              |
| RF02   | Exibir dashboards com gráficos de nota, tipo de comentário, período e unidade.                      | UC05                                    |
| RF03   | Permitir filtragem por unidade, período e palavra-chave nos comentários.                            | UC05, UC08, UC12                        |
| RF04   | Gerar relatórios exportáveis em PDF ou Excel.                                                       | UC06                                    |
| RF05   | Criar alertas automáticos para avaliações negativas ou críticas recorrentes.                        | UC07, UC16                              |
| RF06   | Permitir classificação manual de avaliações e marcação de tags.                                     | UC05 (implícito na interação com dados) |
| RF07   | Comparar desempenho entre unidades (benchmark).                                                     | UC05, UC10                              |
| RF08   | Atualizar dashboards e relatórios dinamicamente com os dados mais recentes.                         | UC05, UC06                              |
| RF09   | Permitir autenticação e controle de acesso baseado em funções (admin, analista, gerente etc.).      | UC01, UC02, UC03, UC04, UC09, UC13      |
| RF10   | Exibir métricas de volume e tendência das avaliações por tema operacional (ex.: fila, atendimento). | UC05                                    |
