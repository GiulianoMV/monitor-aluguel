# Monitor de Aluguéis

![Python](https://img.shields.io/badge/python-3.11%2B-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-Em%20Desenvolvimento-yellow.svg)
![Tests](https://img.shields.io/badge/tests-Pytest-orange.svg)

Coleta de dados imobiliários para análise.

---

## Objetivo

Criado com o objetivo de manter uma base de dados imobiliários, auxiliando na análise de imóveis e tomada de decisões na compra, venda ou aluguel.

---

## Tecnologias Principais

Liste as libs/frameworks usados — só os essenciais:

- **Python 3.11+**
- **Polars**
- **PostgreSQL**
- **Docker**
- **Pytest**
- **YAML**
- **aiohttp / playwright**
- **BeautifulSoup / REGEX**

---

## Estrutura do Projeto

```bash
monitor-aluguel/
│
├── data/                   # Dados de entrada/saída, logs, outputs
├── logs/                   # Logs da aplicação
│
├── src/
│   ├── logger.py           # Serviço de log da aplicação
│   ├── database.py         # Serviço de integração com o banco de dados
│   └── modules/
│       ├── fetcher.py      # Coleta da página HTML
│       ├── parser.py       # Extração dos dados estruturados
│       └── transform.py    # Normalização dos dados extraídos
│
├── tests/                  # Testes unitários e integração
├── settings.yaml           # Arquivo de configuração geral da aplicação
├── requirements.txt        # Dependências
└── run.py                  # Script principal
```

---

## Funcionalidades

Liste apenas as entregas importantes:

1. Coleta multiplataforma

- Realiza a coleta de várias páginas para extração de dados

- Permite a análise de múltiplas fontes, aumentando a abrangência dos resultados.

2. Execução isolada

- Utiliza ambiente virtual + docker

- Evita quebra de dependências por atualização de sistema (servidor) ou manutenções complexas envolvendo o mesmo.

---

## Como Executar

1. Clonar o repositório

```bash
git clone https://github.com/GiulianoMV/monitor-aluguel.com
cd monitor-aluguel
```

2. Criar e ativar ambiente virtual

```bash
python -m venv .venv
source .venv/bin/activate       # Linux/MAC
.venv/Scripts/activate          # Windows
```

3. Instalar dependências

```bash
pip install -r requirements.txt
```

4. Configurações

- Crie um settings.yaml com base no exemplo dado em "settings_example.yaml"

5. Executar o projeto

```bash
python run.py
```

---

## Roadmap

| Etapa | Descrição | Status |
| --- | --- | --- |
| Planejamento | Definição do escopo | 🟨 Em andamento |
| Fetcher | Implementação de coleta | 🔜 Planejado |
| Parser | Implementação de extração | 🔜 Planejado |
| Tranformer | Implementação de limpeza e normalização | 🔜 Planejado |
| Orquestrador | Implementação principal (caller) | 🔜 Planejado |
| Database | Implementação de persistência de dados | 🔜 Planejado |
| Testes | Unidade + integração | 🔜 Planejado |
| Deploy | Docker | 🔜 Planejado |

---

## Contribuição

Passos clássicos:

1. Faça um fork
2. Crie uma branch: git checkout -b feature/nova-feature
3. Commit: git commit -m 'Descrição da mudança'
4. Envie: git push origin feature/nova-feature
5. Abra um Pull Request

---

## Licença

Distribuído sob licença MIT.
Consulte LICENSE para mais detalhes.

---

## Contato

Giuliano Vieira
gmossv603@gmail.com
https://www.linkedin.com/in/giuliano-vieira1/