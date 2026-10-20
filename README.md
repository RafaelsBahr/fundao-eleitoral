# Fundão eleitoral nas eleições de 2026 (RS)

Análise das receitas de campanha dos candidatos do Rio Grande do Sul nas eleições gerais de 2026, com foco no Fundo Especial de Financiamento de Campanha (o "fundão eleitoral"): quanto dinheiro público chegou a cada campanha, por partido, cargo e candidato.

> **Status:** em andamento. Projeto de estudo de engenharia de dados (Python e pandas).

## Perguntas que o projeto quer responder

- Qual parcela do dinheiro das campanhas no RS veio do fundão eleitoral?
- Quais partidos receberam mais recursos do fundão?
- Como os recursos se dividem entre os cargos (deputado estadual, deputado federal, senador, governador)?
- Quais candidatos mais dependeram do fundão?

## Dados

- **Fonte:** Portal de Dados Abertos do TSE, conjunto "Prestação de Contas Eleitorais 2026", recurso "Prestação de contas de candidatos".
- **Download:** https://cdn.tse.jus.br/estatistica/sead/odsele/prestacao_contas/prestacao_de_contas_eleitorais_candidatos_2026.zip
- **Arquivo usado:** `receitas_candidatos_2026_RS.csv` (uma linha por receita de campanha; separador `;`, codificação latin-1).
- **Dicionário das colunas:** `leiame_receitas-candidatos.pdf`, que vem dentro do zip.

Os dados **não estão no repositório**, por causa do tamanho. Para rodar o projeto, baixe o zip, extraia e coloque o `receitas_candidatos_2026_RS.csv` na pasta `data/`.

> Os dados de 2026 ainda são atualizados pelo TSE durante o processo eleitoral. Como a análise é feita em código, basta baixar o arquivo novo e rodar o notebook de novo para atualizar os números.

## Ferramentas

- Python, pandas e Jupyter Notebook
- uv (ambiente e dependências)
- Git e GitHub

## Estrutura

```
fundao-eleitoral/
├── data/          ← dados do TSE (fora do Git)
├── notebooks/     ← análise exploratória
├── pyproject.toml
└── uv.lock
```

## Como rodar

```bash
git clone https://github.com/RafaelsBahr/fundao-eleitoral.git
cd fundao-eleitoral
uv sync
```

Depois, coloque o arquivo de dados em `data/` (ver acima), abra `notebooks/exploracao.ipynb` no VS Code e selecione o kernel `.venv`.

## Autor

Rafael Sedrez Bahr: [github.com/RafaelsBahr](https://github.com/RafaelsBahr)