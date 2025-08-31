# TG-FATEC -  SocialLens
O SocialLens é um sistema inteligente de análise de sentimentos que monitora e interpreta conversas em redes sociais, fornecendo insights valiosos sobre percepção pública, tendências de opinião e comportamento do consumidor

**Projeto:** SocialLens - Sistema de Análise de Sentimentos  
**Aluno:** Sarah Santos Hortiz 
**Data:** 31/08/2025  
**Versão:** 1.0  

---

## ÍNDICE

1. [Características e Funcionalidades Principais](#1-características-e-funcionalidades-principais)
2. [Desenvolvimento em Fases - ADM 1 e ADM 2](#2-desenvolvimento-em-fases---adm-1-e-adm-2)
3. [Fluxos Detalhados por Módulo](#3-fluxos-detalhados-por-módulo)
4. [Resumos Quantitativos](#4-resumos-quantitativos)

---

## 1. CARACTERÍSTICAS E FUNCIONALIDADES PRINCIPAIS

### 1.1 Funcionalidades por Módulo

| **Módulo** | **Funcionalidade** | **Descrição** | **Tipo Usuário** | **Prioridade** | **Versão** |
|------------|-------------------|---------------|------------------|----------------|------------|
| **Autenticação** | Login | Acesso ao sistema com email/senha | Todos | Alta | MVP |
| | Cadastro | Registro de novos usuários | Todos | Alta | MVP |
| | Recuperar Senha | Reset de senha via email | Todos | Média | MVP |
| | Perfil do Usuário | Editar dados pessoais e preferências | Todos | Média | MVP |
| | Logout | Sair do sistema | Todos | Alta | MVP |
| **Home/Dashboard** | Visão Geral | Resumo de métricas principais | Todos | Alta | MVP |
| | Gráficos de Sentimento | Visualização em tempo real | Todos | Alta | MVP |
| | Últimas Análises | Lista das análises recentes | Todos | Média | MVP |
| | Alertas Recentes | Notificações importantes | Todos | Média | MVP |
| | Menu Lateral | Navegação entre módulos | Todos | Alta | MVP |
| | Configurações Rápidas | Atalhos para funções principais | Todos | Baixa | V2 |
| **Configuração** | Adicionar Palavras-chave | Definir termos para monitorar | Todos | Alta | MVP |
| | Gerenciar Hashtags | Adicionar/remover hashtags | Todos | Alta | MVP |
| | Filtros Avançados | Localização, idioma, data | Premium | Média | V2 |
| | Configurar Frequência | Intervalo de coleta de dados | Todos | Média | MVP |
| **Coleta de Dados** | Integração Google Maps | Dados de reviews de estabelecimentos | Sistema | Alta | MVP |
| | Integração Twitter | Buscar tweets via API | Sistema | Alta | V2 |
| | Integração Instagram | Dados simulados/datasets | Sistema | Baixa | V3 |
| | Integração Facebook | Dados simulados/datasets | Sistema | Baixa | V3 |
| | Processamento Real-time | Análise imediata de novos dados | Sistema | Alta | V2 |
| **Análise de Sentimento** | Classificação Básica | Positivo/Neutro/Negativo | Todos | Alta | MVP |
| | Score de Confiança | Percentual de certeza | Todos | Alta | MVP |
| | Detecção de Emoções | Alegria, raiva, medo, etc. | Premium | Média | V2 |
| | Análise de Intensidade | Nível de sentimento (forte/fraco) | Premium | Baixa | V2 |
| **Dashboards** | Gráfico de Pizza | Distribuição de sentimentos | Todos | Alta | MVP |
| | Gráfico de Linhas | Evolução temporal | Todos | Alta | MVP |
| | Gráfico de Barras | Comparação por período | Todos | Média | MVP |
| | Mapa de Calor | Intensidade por região | Premium | Baixa | V2 |
| | Word Cloud | Palavras mais mencionadas | Todos | Média | MVP |
| **Relatórios** | Relatório Diário | Resumo das últimas 24h | Todos | Média | MVP |
| | Relatório Semanal | Análise da semana | Todos | Média | MVP |
| | Relatório Customizado | Período personalizado | Premium | Baixa | V2 |
| | Exportar PDF | Download de relatórios | Todos | Média | MVP |
| | Exportar Excel | Dados em planilha | Premium | Baixa | V2 |
| **Sistema de Alertas** | Alerta por Email | Notificações via email | Todos | Média | MVP |
| | Configurar Limites | Definir quando alertar | Todos | Média | MVP |
| | Alertas de Crise | Detecção de sentimento muito negativo | Premium | Alta | V2 |
| | Alertas de Oportunidade | Sentimento muito positivo | Premium | Média | V2 |
| | Histórico de Alertas | Log de todas as notificações | Todos | Baixa | V2 |

### 1.2 Tipos de Usuário

| **Tipo** | **Descrição** | **Funcionalidades** | **Limitações** |
|----------|---------------|---------------------|----------------|
| **Gratuito** | Usuário básico | Dashboard básico, 1 projeto, alertas limitados | 500 posts/mês, relatórios simples |
| **Premium** | Usuário pago | Múltiplos projetos, relatórios avançados, API | Sem limitações principais |
| **Admin** | Administrador | Gerenciar sistema, usuários, logs | Acesso total |

### 1.3 Resumo por Prioridade

| **Prioridade** | **Quantidade** | **% do Total** | **Versão Alvo** |
|----------------|----------------|----------------|-----------------|
| **Alta** | 18 funcionalidades | 40% | MVP |
| **Média** | 19 funcionalidades | 42% | MVP/V2 |
| **Baixa** | 8 funcionalidades | 18% | V2/V3 |
| **TOTAL** | **45 funcionalidades** | **100%** | **3 versões** |

---

## 2. DESENVOLVIMENTO EM FASES - ADM 1 E ADM 2

### 2.1 Comparativo das Fases

| **Característica** | **ADM 1 (Maps)** | **ADM 2 (Twitter)** |
|-------------------|------------------|---------------------|
| **Fonte de Dados** | Simulada/Local | Real/API |
| **Volume** | ~1000 registros | ~10k+ tweets/dia |
| **Atualização** | Estática | Tempo real |
| **Complexidade** | Baixa | Média |
| **Geolocalização** | 100% dos dados | ~5% dos tweets |
| **Validação** | Conceito | Produto real |
| **Duração** | 6-8 semanas | 8-10 semanas |
| **Esforço** | 130 horas | 180 horas |
| **Risco** | Baixo | Médio |

### 2.2 Funcionalidades por Fase

#### ADM 1 - Google Maps + Análise Básica

| **Módulo** | **Funcionalidade** | **Descrição** | **Prioridade** | **Semanas** |
|------------|-------------------|---------------|----------------|-------------|
| **Autenticação** | Sistema de Login/Cadastro | Admin único para testes | Alta | 1 |
| **Dashboard Básico** | Interface Principal | Layout responsivo simples | Alta | 1 |
| **Google Maps Integration** | Mapa Interativo | Visualizar pontos de dados | Alta | 2 |
| **Dados Simulados** | Dataset de Reviews | Dados locais de estabelecimentos | Alta | 1 |
| **Análise de Sentimentos** | Modelo Básico (TextBlob) | Classificação Positivo/Neutro/Negativo | Alta | 2 |
| **Visualização** | Marcadores no Mapa | Cores por sentimento | Alta | 1 |

#### ADM 2 - Twitter Integration

| **Módulo** | **Funcionalidade** | **Descrição** | **Prioridade** | **Semanas** |
|------------|-------------------|---------------|----------------|-------------|
| **Twitter API** | Coleta de Tweets | Buscar por palavras-chave/hashtags | Alta | 2 |
| **Processamento RT** | Pipeline de Dados | Limpeza e análise em tempo real | Alta | 2 |
| **Geolocalização** | Tweets com Coordenadas | Filtrar tweets geolocalizados | Alta | 1 |
| **Dashboard Avançado** | Gráficos Dinâmicos | Charts.js/Recharts | Média | 2 |
| **Sistema de Monitoramento** | Palavras-chave Config | CRUD de termos a monitorar | Média | 1 |
| **Histórico** | Armazenar Dados | Banco de dados persistente | Alta | 1 |

### 2.3 Tecnologias por Fase

| **Componente** | **ADM 1** | **ADM 2** |
|----------------|-----------|-----------|
| **Frontend** | React + Google Maps API | React + Charts + Filtros |
| **Backend** | Python Flask básico | Python Flask + Celery |
| **Banco de Dados** | SQLite local | PostgreSQL |
| **IA/ML** | TextBlob (simples) | Hugging Face BERT |
| **APIs Externas** | Google Maps | Google Maps + Twitter |
| **Hospedagem** | Local/GitHub Pages | Railway/Render (gratuito) |

### 2.4 Cronograma Detalhado

#### FASE 1 - ADM 1 (6-8 semanas)

| **Semana** | **Atividades** | **Entregáveis** | **Esforço (h)** |
|------------|----------------|-----------------|-----------------|
| 1 | Setup ambiente + Auth + Dashboard básico | Login funcional + Interface | 20h |
| 2 | Integração Google Maps + Dados simulados | Mapa com marcadores | 25h |
| 3-4 | Análise de sentimentos + Visualização | Cores por sentimento | 50h |
| 5-6 | Refinamentos + Testes + Documentação | ADM 1 completo | 35h |
| **Total** | **6 semanas** | **Sistema funcional** | **130h** |

#### FASE 2 - ADM 2 (8-10 semanas)

| **Semana** | **Atividades** | **Entregáveis** | **Esforço (h)** |
|------------|----------------|-----------------|-----------------|
| 1-2 | Twitter API + Pipeline de dados | Coleta funcionando | 60h |
| 3-4 | Processamento RT + Geolocalização | Tweets no mapa | 50h |
| 5-6 | Dashboard avançado + Gráficos | Interface completa | 40h |
| 7-8 | Sistema de monitoramento + Filtros | Configuração dinâmica | 30h |
| **Total** | **8 semanas** | **Sistema completo** | **180h** |

---

## 3. FLUXOS DETALHADOS POR MÓDULO

### 3.1 ADM 1 - Módulo de Autenticação

| **Funcionalidade** | **Fluxo do Usuário** | **Ações do Sistema** | **Telas/Componentes** | **Dados Envolvidos** | **Prioridade** |
|-------------------|---------------------|---------------------|----------------------|---------------------|----------------|
| **Cadastro** | 1. Acessa página inicial<br>2. Clica "Cadastrar"<br>3. Preenche formulário<br>4. Confirma criação | 1. Valida dados<br>2. Verifica email único<br>3. Hash da senha<br>4. Salva no BD<br>5. Redireciona para login | • Tela de Cadastro<br>• Formulário responsivo<br>• Validações em tempo real | • Nome completo<br>• Email<br>• Senha<br>• Confirmação senha | Alta |
| **Login** | 1. Insere email/senha<br>2. Clica "Entrar"<br>3. Aguarda autenticação<br>4. Redirecionado para dashboard | 1. Valida credenciais<br>2. Gera token/sessão<br>3. Armazena sessão<br>4. Redireciona usuário | • Tela de Login<br>• Formulário simples<br>• Mensagens de erro | • Email<br>• Senha<br>• Token de sessão | Alta |
| **Logout** | 1. Clica botão "Sair"<br>2. Confirma ação<br>3. Redirecionado para login | 1. Destrói sessão<br>2. Limpa tokens<br>3. Limpa cache local | • Header com botão<br>• Modal de confirmação | • Token de sessão | Alta |

### 3.2 ADM 1 - Módulo Dashboard

| **Funcionalidade** | **Fluxo do Usuário** | **Ações do Sistema** | **Telas/Componentes** | **Dados Envolvidos** | **Prioridade** |
|-------------------|---------------------|---------------------|----------------------|---------------------|----------------|
| **Visão Geral** | 1. Login realizado<br>2. Carregamento automático<br>3. Visualiza métricas<br>4. Navega entre seções | 1. Carrega dados simulados<br>2. Calcula estatísticas<br>3. Renderiza componentes<br>4. Atualiza cache | • Dashboard principal<br>• Cards de métricas<br>• Gráficos básicos | • Total de reviews<br>• % sentimentos<br>• Médias por região | Alta |
| **Navegação** | 1. Menu lateral disponível<br>2. Clica em seções<br>3. Transição entre telas<br>4. Breadcrumbs visíveis | 1. Roteamento SPA<br>2. Carregamento lazy<br>3. Histórico de navegação<br>4. Estado persistido | • Sidebar responsiva<br>• Menu hambúrguer (mobile)<br>• Breadcrumbs | • Rotas ativas<br>• Estado da navegação<br>• Cache de páginas | Alta |

### 3.3 ADM 1 - Módulo Google Maps

| **Funcionalidade** | **Fluxo do Usuário** | **Ações do Sistema** | **Telas/Componentes** | **Dados Envolvidos** | **Prioridade** |
|-------------------|---------------------|---------------------|----------------------|---------------------|----------------|
| **Carregar Mapa** | 1. Acessa seção "Mapa"<br>2. Aguarda carregamento<br>3. Visualiza região padrão<br>4. Interage com controles | 1. Carrega Google Maps API<br>2. Define coordenadas iniciais<br>3. Aplica configurações<br>4. Renderiza marcadores | • Componente de Mapa<br>• Controles de zoom<br>• Botões de tipo de mapa | • API Key Google<br>• Coordenadas centro<br>• Nível de zoom<br>• Dados de reviews | Alta |
| **Visualizar Marcadores** | 1. Observa pontos no mapa<br>2. Identifica cores (sentimentos)<br>3. Clica em marcador<br>4. Lê informações detalhadas | 1. Processa dados reviews<br>2. Calcula sentimentos<br>3. Define cores por sentimento<br>4. Cria InfoWindows | • Marcadores coloridos<br>• InfoWindows customizadas<br>• Clusters (opcional) | • Coordenadas lat/lng<br>• Texto das reviews<br>• Score de sentimento<br>• Dados estabelecimento | Alta |
| **Filtrar Dados** | 1. Usa controles de filtro<br>2. Seleciona categorias<br>3. Define período<br>4. Aplica filtros | 1. Filtra dataset<br>2. Remove/adiciona marcadores<br>3. Atualiza estatísticas<br>4. Mantém estado filtro | • Painel de filtros<br>• Checkboxes/Selects<br>• Botões aplicar/limpar | • Categorias selecionadas<br>• Range de datas<br>• Tipos de sentimento | Média |

### 3.4 ADM 2 - Módulo Twitter API

| **Funcionalidade** | **Fluxo do Usuário** | **Ações do Sistema** | **Telas/Componentes** | **Dados Envolvidos** | **Prioridade** |
|-------------------|---------------------|---------------------|----------------------|---------------------|----------------|
| **Configurar Monitoramento** | 1. Acessa "Configurações"<br>2. Adiciona palavras-chave<br>3. Define filtros<br>4. Salva configuração<br>5. Inicia monitoramento | 1. Valida keywords<br>2. Configura API Twitter<br>3. Define parâmetros busca<br>4. Salva no BD<br>5. Inicia job coleta | • Tela de configuração<br>• Formulário keywords<br>• Toggles de filtros<br>• Status do monitoramento | • Lista de keywords<br>• Filtros de idioma<br>• Raio geográfico<br>• Configurações API | Alta |
| **Coletar Tweets** | 1. Sistema coleta automaticamente<br>2. Usuário vê contador em tempo real<br>3. Observa novos tweets no mapa<br>4. Monitora logs de coleta | 1. Chama Twitter API<br>2. Processa rate limits<br>3. Filtra tweets relevantes<br>4. Salva no BD<br>5. Dispara processamento | • Dashboard tempo real<br>• Contador de tweets<br>• Log de atividades<br>• Status da API | • Tweets JSON<br>• Metadados autor<br>• Coordenadas (se disponível)<br>• Timestamps | Alta |
| **Processar Geolocalização** | 1. Visualiza tweets no mapa<br>2. Filtra por região<br>3. Analisa concentrações<br>4. Compara com dados Maps | 1. Extrai coordenadas<br>2. Valida precisão<br>3. Aplica no mapa<br>4. Calcula clusters<br>5. Integra com dados existentes | • Marcadores Twitter (diferenciados)<br>• Filtros por fonte<br>• Layers do mapa<br>• Clustering inteligente | • Coordenadas lat/lng<br>• Precisão GPS<br>• Localização inferida<br>• Dados combinados | Média |

### 3.5 Fluxos Principais Integrados

#### FLUXO 1: Setup Inicial - ADM 1

| **Passo** | **Usuário** | **Sistema** | **Duração** | **Resultado** |
|-----------|-------------|-------------|-------------|---------------|
| 1 | Acessa sistema primeira vez | Apresenta tela de cadastro | 30s | Usuário na tela de registro |
| 2 | Preenche dados cadastro | Valida e cria conta | 2min | Conta criada, redirecionado login |
| 3 | Faz login no sistema | Autentica e gera sessão | 15s | Usuário autenticado |
| 4 | Visualiza dashboard inicial | Carrega dados simulados | 5s | Dashboard com métricas básicas |
| 5 | Navega para mapa | Inicializa Google Maps | 3s | Mapa carregado com marcadores |
| 6 | Explora funcionalidades | Processa interações | 10min | Usuário familiarizado |

#### FLUXO 2: Configuração Twitter - ADM 2

| **Passo** | **Usuário** | **Sistema** | **Duração** | **Resultado** |
|-----------|-------------|-------------|-------------|---------------|
| 1 | Acessa configurações | Carrega interface config | 2s | Tela de configuração |
| 2 | Adiciona palavras-chave | Valida e salva termos | 1min | Keywords configuradas |
| 3 | Define filtros geográficos | Configura parâmetros API | 30s | Filtros aplicados |
| 4 | Inicia monitoramento | Ativa coleta Twitter | 5s | Jobs iniciados |
| 5 | Monitora coleta em tempo real | Processa tweets incoming | Contínuo | Dados alimentando sistema |

---

## 4. RESUMOS QUANTITATIVOS

### 4.1 Complexidade por Fase

#### ADM 1 - Complexidade

| **Módulo** | **Funcionalidades** | **Telas** | **Componentes** | **APIs** | **Complexidade** |
|------------|-------------------|-----------|-----------------|----------|------------------|
| Autenticação | 3 | 2 | 5 | 0 | Baixa |
| Dashboard | 2 | 1 | 8 | 0 | Baixa |
| Google Maps | 3 | 1 | 12 | 1 | Média |
| Análise Sentimentos | 2 | 0 | 4 | 0 | Média |
| **TOTAL ADM 1** | **10** | **4** | **29** | **1** | **Baixa-Média** |

#### ADM 2 - Complexidade

| **Módulo** | **Funcionalidades** | **Telas** | **Componentes** | **APIs** | **Complexidade** |
|------------|-------------------|-----------|-----------------|----------|------------------|
| Twitter API | 3 | 1 | 8 | 1 | Alta |
| Dashboard Avançado | 2 | 1 | 15 | 0 | Média |
| Monitoramento | 2 | 1 | 10 | 0 | Média |
| **TOTAL ADM 2** | **7** | **3** | **33** | **1** | **Média-Alta** |
| **TOTAL GERAL** | **17** | **7** | **62** | **2** | **Média** |

### 4.2 Estimativa de Desenvolvimento

#### ADM 1 (6-8 semanas)

| **Sprint** | **Semanas** | **Funcionalidades** | **Esforço** | **Risco** |
|------------|-------------|-------------------|-------------|-----------|
| Sprint 1 | 1-2 | Auth + Dashboard básico | 40h | Baixo |
| Sprint 2 | 3-4 | Google Maps + Dados simulados | 50h | Médio |
| Sprint 3 | 5-6 | Análise sentimentos + UI final | 40h | Baixo |
| **Total** | **6** | **10 funcionalidades** | **130h** | **Baixo** |

#### ADM 2 (8-10 semanas)

| **Sprint** | **Semanas** | **Funcionalidades** | **Esforço** | **Risco** |
|------------|-------------|-------------------|-------------|-----------|
| Sprint 4 | 7-8 | Twitter API + Pipeline | 60h | Alto |
| Sprint 5 | 9-10 | Dashboard avançado | 50h | Médio |
| Sprint 6 | 11-12 | Sistema monitoramento | 40h | Médio |
| Sprint 7 | 13-14 | Integração e testes | 30h | Médio |
| **Total** | **8** | **7 funcionalidades** | **180h** | **Médio** |

### 4.3 Recursos Tecnológicos (100% Gratuitos)

| **Categoria** | **ADM 1** | **ADM 2** | **Observações** |
|---------------|-----------|-----------|-----------------|
| **APIs** | Google Maps (gratuita) | Google Maps + Twitter API v2 Essential | 500k tweets/mês grátis |
| **Frontend** | React + Maps API | React + Charts + Filtros | Todas as bibliotecas gratuitas |
| **Backend** | Python Flask básico | Python Flask + Celery | Processamento assíncrono |
| **Banco de Dados** | SQLite local | PostgreSQL local | Sem custos de cloud |
| **Hospedagem** | GitHub Pages | Railway/Render (tier gratuito) | Pode ter limitações de uptime |
| **IA/ML** | TextBlob | Hugging Face (modelos gratuitos) | BERT, RoBERTa disponíveis |
| **Custo Total** | **R$ 0,00** | **R$ 0,00** | **Completamente gratuito** |

### 4.4 Métricas de Sucesso

| **Tipo** | **Métrica** | **ADM 1** | **ADM 2** | **Meta Final** |
|----------|-------------|-----------|-----------|----------------|
| **Técnica** | Precisão Análise Sentimentos | 75% | 85% | 85%+ |
| **Performance** | Tempo de Carregamento | < 3s | < 5s | < 3s |
| **Usabilidade** | Taxa de Conclusão Tarefas | 90% | 85% | 90%+ |
| **Funcional** | Uptime do Sistema | 95% | 99% | 99%+ |
| **Volume** | Dados Processados | 1k registros | 10k+ tweets/dia | Escalável |

---

## CONCLUSÃO

Este documento apresenta as tabelas completas para o desenvolvimento do SocialLens em duas fases distintas. A abordagem gradual permite:

1. **Validação rápida do conceito** com ADM 1 (Google Maps)
2. **Expansão controlada** com ADM 2 (Twitter Integration)
3. **Desenvolvimento com custo zero** utilizando apenas recursos gratuitos
4. **Metodologia ágil** com sprints bem definidos
5. **Arquitetura escalável** preparada para futuras expansões

**Total do Projeto:** 16 semanas | 17 funcionalidades | 310 horas | Investimento R$ 0,00

---

**Observação:** Este documento serve como guia técnico e gerencial para o desenvolvimento do SocialLens. Pode ser utilizado para apresentações acadêmicas, estimativas de projeto e acompanhamento de desenvolvimento.

---

*Documento gerado em [31/08/2025] | Versão 1.0 | Projeto SocialLens*
