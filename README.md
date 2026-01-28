# 🤖 Tradar BOT - Sistema de Trading Quantitativo V3.0

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Status](https://img.shields.io/badge/status-production%20ready-green)
![Versão](https://img.shields.io/badge/version-3.0--quantitativo-orange)
![Licença](https://img.shields.io/badge/license-MIT-lightgrey)
![GitHub](https://img.shields.io/github/repo-size/Teo986L/Tradar_BOT)

**Sistema automatizado de trading multi-ativo com hierarquia temporal, ignição dinâmica e proteção de risco zero.**

## 🚀 Visão Geral

Tradar BOT é uma solução completa de trading automatizado que combina análise técnica multi-timeframe com gestão de risco avançada. O sistema opera 8 classes de ativos simultaneamente usando estratégias baseadas em confluência de indicadores e protocolos de proteção automática.

### ✨ Características Principais

✅ **Sistema Multi-Ativo**: Forex, Criptomoedas, Commodities, Índices  
✅ **Hierarquia Temporal 24H/4H/5M**: Filtros de exaustão + tendência principal + execução  
✅ **Ignição Dinâmica**: Entradas validadas por ADX + RSI + ATR  
✅ **Risco Zero Automático**: Free-trade ativado em níveis de exaustão  
✅ **Painel Quantitativo**: KPIs avançados, análise estatística, sugestões inteligentes  
✅ **Protocolos de Emergência**: Stop total, reset de mercado, proteção de capital  

## 📦 Instalação Rápida

```bash
# Clone o repositório
git clone https://github.com/Teo986L/Tradar_BOT.git
cd Tradar_BOT

# Instale as dependências
pip install pandas numpy pandas-ta

# Execute o sistema
python main.py

 Ativos Disponíveis

XAUUSD    # Ouro/USD          (commodity)
BTCUSD    # Bitcoin/USD       (cripto)
EURUSD    # Euro/USD          (forex)
ETHUSD    # Ethereum/USD      (cripto)
GBPUSD    # Libra/USD         (forex)
US500     # S&P 500           (índice)
NAS100    # NASDAQ 100        (índice)
OIL       # Petróleo          (commodity)


Comandos Básicos

# Adicionar ativo para operação
adicionar BTCUSD 10000

# Ver status detalhado
status XAUUSD

# Iniciar ciclo automático (60 segundos)
iniciar 60

# Painel quantitativo completo
resumo

🎯 Estratégia de Trading
Hierarquia Temporal

24H (Filtro) → Exaustão diária (RSI >75/<25)
   ↓
4H (Tendência) → Direção principal (MACD + ADX)
   ↓
5M (Execução) → Gatilho de entrada + gerenciamento


Regras de Entrada (Ignição)
ADX 4H > 25 - Mercado com força direcional

RSI 5M entre 40-60 - Zona neutra para entrada

Sem exaustão 24H - RSI diário fora dos extremos

Confluência temporal - Alinhamento 4H + 5M

Sistema de Saída
Take Profit Dinâmico: 1.5x a 3.0x ATR (por ativo)

Risco Zero Automático: SL move para entrada em RSI 5M >70/<30

Exaustão Temporal: Saída após tempo limite configurável

Stop Loss Protegido: Baseado em ATR + condições de mercado

📊 Sistema de Proteção
Protocolos de Emergência

Protocolo	Condição	Ação
Stop Total	Drawdown > 15%	Fecha todas posições, bloqueia 24h
Reset de Mercado	3 stops seguidos	Remove ativo, aguarda 4h
Proteção Capital	Capital < 70%	Reduz risco para 1%, limita operações

Alertas Automáticos
🔔 Nível 1 (Crítico): Stop loss, queda de conexão

⚠️ Nível 2 (Importante): Risco zero ativado, nova posição

📊 Nível 3 (Informativo): Sinais fortes, exaustão detectada

🏗️ Estrutura do Projeto
Tradar_BOT/
├── main.py                    # Ponto de entrada principal
├── bot_trader.py             # Classe principal do bot (BotTraderPro)
├── trading_interface.py      # Interface de controle multi-bot
├── requirements.txt          # Dependências do projeto
├── logs/                     # Logs e estatísticas automáticas
│   ├── operacoes_*.json
│   └── estatisticas_*.json
├── backups/                  # Backups de configuração
│   └── trading_config_*.json
└── README.md                # Este arquivo

🎮 Comandos Completos
          Comando	                      Descrição	                 Exemplo
adicionar [ATIVO] [CAPITAL]	      Adiciona novo ativo	      adicionar XAUUSD 15000
_____________________________________________________________________
 remover [ATIVO]	              Remove ativo da operação	      remover BTCUSD
________________________________________________________________________
listar	Lista ativos disponíveis	listar
_____________________________________________________________________
status [ATIVO]	Status técnico completo	status EURUSD
________________________________________________________________________
iniciar [INTERVALO]	Inicia ciclo automático	iniciar 60
______________________________________________________________________
parar	Para o ciclo automático	parar
______________________________________________________________________
resumo	Painel quantitativo completo	resumo
____________________________________________________________________
analisar [ATIVO]	Análise profunda de desempenho	analisar BTCUSD
___________________________________________________________________
salvar	Salva configuração atual	salvar
___________________________________________________________________
carregar	Carrega configuração salva	carregar
_______________________________________________________________________
exemplo	Executa demonstração (30s)	exemplo
_____________________________________________________________________
sair	Sai do sistema	sair
___________________________________________________________________


📈 Métricas Monitoradas
KPIs Principais
Expectativa Matemática: Lucro médio por operação

Taxa de Ignição: % entradas com ADX validado

Eficiência Proteção: % operações que atingiram risco zero

Win Rate: Percentual de operações lucrativas

Drawdown Máximo: Maior perda acumulada

Tempo Médio/Op: Eficiência temporal

Relatórios Automáticos
📋 Diário: 18:00 - Operações do dia, P/L, alertas

📋 Semanal: Segunda 09:00 - Performance vs meta, sugestões

📋 Mensal: Primeiro dia útil - Retorno acumulado, ajustes

🔧 Tecnologias Utilizadas
Python 3.8+: Linguagem principal

pandas & numpy: Análise de dados

pandas-ta: Indicadores técnicos

asyncio: Execução assíncrona

JSON: Armazenamento de configuração

🤝 Contribuindo
Contribuições são bem-vindas! Siga estes passos:

Fork o projeto

Crie uma branch (git checkout -b feature/NovaFuncionalidade)

Commit suas mudanças (git commit -m 'Adiciona nova funcionalidade')

Push para a branch (git push origin feature/NovaFuncionalidade)

Abra um Pull Request

Diretrizes
✅ Teste em conta demo antes de enviar

✅ Documente novas funcionalidades

✅ Mantenha compatibilidade com versões existentes

✅ Adicione testes quando possível

📄 Licença
Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.

⚠️ Aviso Legal
ESTE SOFTWARE É PARA FINS EDUCACIONAIS E DE PESQUISA.

Trading envolve riscos significativos de perda financeira

Teste exaustivamente em conta demo antes de usar capital real

O desenvolvedor não se responsabiliza por perdas financeiras

Você é responsável por entender e gerenciar seus próprios riscos

NUNCA USE DINHEIRO QUE VOCÊ NÃO PODE PERDER.

📞 Suporte
Canais de Ajuda
📖 Documentação: Consulte o Manual Completo

🐛 Issues: Reporte problemas no GitHub Issues

💬 Discussões: Tire dúvidas na aba Discussions

Níveis de Suporte
🟢 Básico: Dúvidas de uso, configuração inicial

🟡 Técnico: Problemas com execução, bugs

🔴 Emergência: Situações críticas (perda de conexão, bugs graves)

🎯 Próximas Atualizações Planejadas
Conexão com APIs de corretoras reais

Backtesting integrado com histórico

Interface web com gráficos em tempo real

Machine learning para ajuste automático de parâmetros

Alertas via Telegram/WhatsApp integrados

<div align="center">
💙 Se este projeto te ajudou, considere dar uma estrela!
⭐ Star no GitHub

Versão: 3.0 Quantitativo | Última atualização: Janeiro 2024
Autor: Teo986L | Contribuições: Abertas

</div> ```


📁 Arquivos Adicionais para Criar no Repositório
1. .gitignore

# Dados sensíveis e configurações
*.json
!requirements.txt

# Logs e backups
logs/
backups/
*.log
*.csv

# Ambiente Python
__pycache__/
*.py[cod]
*$py.class
.Python
env/
venv/
.venv/

# IDEs
.vscode/
.idea/
*.swp
*.swo

# Sistema operacional
.DS_Store
Thumbs.db

2. requirements.txt
pandas>=2.0.0
numpy>=1.24.0
pandas-ta>=0.3.14

4. LICENSE (MIT License)
MIT License

Copyright (c) 2026 Teo986L

Permission is hereby granted...

