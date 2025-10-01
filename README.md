👤 Autor
Mateus Teni Pierro

RM555125

# 🚀 Mottu Management - IoT & Database Project

Projeto desenvolvido como parte da disciplina **Mastering Relational and Non-Relational Database**.  
Integra conceitos de **IoT, MQTT, Oracle Database e Dashboards** para simulação e gerenciamento de frotas de drones/motos em áreas isoladas.

---

## 📂 Estrutura do Projeto

mottu-management/
│-- publisher_sim.py # Publicador MQTT (simula dispositivos)
│-- subscriber_mqtt.py # Subscriber que grava dados em banco
│-- streamlit_app.py # Dashboard interativo com Streamlit
│-- demo_run.py # Script de execução de teste
│-- docker-compose.yml # Serviços Docker (Mosquitto, etc.)
│-- mosquitto.conf # Configuração do broker MQTT
│-- telemetry.db # Banco de dados SQLite (exemplo)
│-- requirements.txt # Dependências Python
│-- README.md # Este arquivo :)
└── docs/
└── 2TDSX_2024_Proj_BD.pdf # Documentação técnica (PDF)
└── 2TDSX_2024_CodigoSql_Integrantes.sql # Scripts SQL Oracle

yaml
Copy code

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.9+**
- **Paho MQTT** (comunicação IoT)
- **SQLite** (exemplo local) / **Oracle Database** (SQL relacional)
- **Docker + Mosquitto** (broker MQTT)
- **Streamlit** (dashboard de visualização)
- **PL/SQL** (procedures, functions, triggers)

---

## ⚙️ Pré-requisitos

- [Python 3.9+](https://www.python.org/downloads/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Oracle SQL Developer (para execução dos scripts PL/SQL)
- Pip / Virtualenv para instalar dependências

---

## ▶️ Como Rodar o Projeto

### 1️⃣ Clonar o repositório
```bash
git clone https://github.com/seu-usuario/mottu-management.git
cd mottu-management
2️⃣ Criar ambiente virtual e instalar dependências
bash
Copy code
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

pip install -r requirements.txt
3️⃣ Subir o broker MQTT com Docker
bash
Copy code
docker-compose up -d
4️⃣ Iniciar o subscriber (consome mensagens e grava no banco)
bash
Copy code
python subscriber_mqtt.py
5️⃣ Rodar o publisher (simula os dispositivos enviando dados)
bash
Copy code
python publisher_sim.py
6️⃣ Abrir o dashboard Streamlit
bash
Copy code
streamlit run streamlit_app.py
🗄️ Banco de Dados Oracle
Scripts estão no arquivo:
📜 docs/2TDSX_2024_CodigoSql_Integrantes.sql

Inclui:

CREATE TABLE com inserts (≥5 registros por tabela)

2 Procedimentos PL/SQL

2 Funções PL/SQL

1 Trigger de Auditoria

📊 Funcionalidades
Publicação de telemetria de dispositivos (drones/motos).

Consumo de mensagens MQTT e persistência em banco.

Conversão de dados relacionais para JSON manualmente.

Dashboard interativo com posições, status e bateria.

Auditoria automática via Trigger.

Tratamento de exceções em todas as funções e procedimentos.

🧪 Exemplo de Execução
Simulação MQTT
csharp
Copy code
[SUBSCRIBER] Aguardando mensagens...
[BACKEND] saved moto-001 at 2025-09-30T13:39:20.875767
[BACKEND] saved moto-002 at 2025-09-30T13:39:20.879736
[BACKEND] saved moto-003 at 2025-09-30T13:39:20.882783
Dashboard (Streamlit)
📷 [Inserir aqui prints do dashboard com mapa e tabelas]

