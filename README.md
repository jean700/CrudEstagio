# 🎓 UniFil — Sistema de Gestão de Salas e Laboratórios

[![Python](https://img.shields.io/badge/Python-3.10%2B-F15A24?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Gradio](https://img.shields.io/badge/Gradio-4.0%2B-F15A24?style=flat-square&logo=gradio&logoColor=white)](https://gradio.app/)
[![SQLite](https://img.shields.io/badge/SQLite-3-F15A24?style=flat-square&logo=sqlite&logoColor=white)](https://www.sqlite.org/)

Aplicação web desenvolvida para o controle e agendamento de espaços físicos do **Centro Universitário UniFil** (Londrina - PR). O sistema gerencia as **Salas de Aula (1026 a 1040)** do Bloco Central e os **Laboratórios (1 a 8)** do Bloco de Tecnologia.

---

## 🚀 Funcionalidades

- **🔐 Autenticação e Níveis de Acesso (RBAC):**
  - **Professor:** Consulta salas/laboratórios disponíveis e realiza reservas de horários.
  - **Coordenador:** Possui acesso ao painel administrativo exclusivo para cadastrar e excluir espaços físicos.
- **📅 Prevenção Anti-Choque de Horários:** Validação automática que impede agendamentos duplicados na mesma sala, data e período (Manhã, Tarde ou Noite).
- **🏢 População Automática:** Inicialização automática do banco de dados com todas as salas (1026-1040) e laboratórios (1-8) da UniFil.
- **🔍 Filtros e Buscas:** Pesquisa dinâmica por tipo de espaço e número/nome da sala.
- **🎨 Identidade Visual Institucional:** Interface customizada na cor **Laranja UniFil (`#F15A24`)**.

---

## 📂 Estrutura do Repositório

```text
unifil-controle-salas/
├── app.py              # Interface gráfica Gradio e lógica principal
├── database.py         # Configuração do SQLite e população inicial
├── requirements.txt    # Dependências do projeto Python
├── .gitignore          # Arquivos ignorados pelo Git
└── README.md           # Documentação do projeto
git clone [https://github.com/SEU-USUARIO/unifil-controle-salas.git](https://github.com/SEU-USUARIO/unifil-controle-salas.git)
cd unifil-controle-salas
python -m venv venv
# No Windows:
venv\Scripts\activate
# No Linux/Mac:
source venv/bin/activate
pip install -r requirements.txt
python app.py
