# 🗺️ SocialLens

**Sistema de Análise de Sentimentos em Redes Sociais com Visualização Geográfica**

[![Status](https://img.shields.io/badge/Status-Planning-blue.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Language](https://img.shields.io/badge/Language-Python-yellow.svg)]()
[![Framework](https://img.shields.io/badge/Frontend-React-blue.svg)]()

## 🎯 Sobre o Projeto

O SocialLens é um sistema inteligente que monitora e analisa sentimentos em redes sociais, fornecendo insights valiosos através de visualizações geográficas interativas. Combina análise de dados, inteligência artificial e geolocalização para entregar informações estratégicas sobre percepção pública e comportamento do consumidor.

## ✨ Principais Funcionalidades

- 🗺️ **Visualização Geográfica**: Mapas interativos com dados de sentimento
- 🤖 **Análise de IA**: Processamento de linguagem natural para classificação de sentimentos
- 📱 **Integração Social**: Coleta de dados do Twitter, Google Maps, Instagram e Facebook
- 📊 **Dashboards Dinâmicos**: Gráficos e métricas em tempo real
- 🚨 **Sistema de Alertas**: Notificações automáticas para mudanças significativas
- 📄 **Relatórios Automatizados**: Exports em PDF e Excel

## 🚀 Fases de Desenvolvimento

### 📍 ADM 1: Google Maps + Análise Básica (6-8 semanas)
- ✅ Sistema de autenticação
- ✅ Dashboard básico com métricas
- ✅ Integração Google Maps
- ✅ Análise de sentimentos (TextBlob)
- ✅ Dados simulados de reviews
- ✅ Visualização com marcadores coloridos

### 🐦 ADM 2: Twitter Integration (8-10 semanas)
- ✅ Integração Twitter API v2
- ✅ Processamento em tempo real
- ✅ Dashboard avançado com gráficos
- ✅ Sistema de monitoramento de keywords
- ✅ Análise de sentimentos aprimorada (BERT)
- ✅ Geolocalização de tweets

## 🛠️ Stack Tecnológica

| Categoria | ADM 1 | ADM 2 |
|-----------|-------|-------|
| **Frontend** | React + Google Maps API | React + Chart.js + Filtros |
| **Backend** | Python Flask | Python Flask + Celery |
| **Database** | SQLite | PostgreSQL |
| **AI/ML** | TextBlob | Hugging Face BERT |
| **Hosting** | GitHub Pages | Railway/Render (free) |

## 💰 Estratégia Zero-Cost

- 🆓 **APIs Gratuitas**: Twitter API Essential (500k tweets/mês)
- 🆓 **Hospedagem**: GitHub Pages + Railway/Render
- 🆓 **IA/ML**: Hugging Face models + TextBlob  
- 🆓 **Banco de Dados**: PostgreSQL local/SQLite
- 🆓 **Ferramentas**: VS Code, Git, Figma

## 📊 Métricas de Sucesso

- 🎯 Precisão de análise: **85%+**
- ⚡ Performance: **< 3s loading**
- 📈 Uptime: **99%+**
- 👥 Satisfação usuário: **4.0+/5.0**

## 🗂️ Estrutura do Projeto

docs/           # Documentação completa
src/            # Código fonte
├── frontend/   # React application
├── backend/    # Python Flask API
└── data/       # Datasets e modelos
tests/          # Testes automatizados

## 🚦 Como Executar

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/sociallens.git

# ADM 1 - Desenvolvimento local
cd sociallens
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py

# Frontend
cd frontend
npm install
npm start

📄 Licença
Este projeto está sob a licença MIT. Veja LICENSE para mais detalhes.

👤 Autor
Sarah Santos Hortiz