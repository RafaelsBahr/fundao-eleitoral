# Fundão eleitoral nas eleições de 2026 (RS)

Projeto de estudo para praticar o que aprendi recentemente de Python e pandas, usando uma base de dados real e recente: as receitas de campanha dos candidatos do Rio Grande do Sul em 2026, com foco no Fundo Especial de Financiamento de Campanha (o "fundão eleitoral").

> **Status:** concluído (15 exercícios em 3 níveis).

## O que eu descobri

Números calculados com o arquivo do TSE baixado em 18/10/2026.

- **O fundão é a maior parte do dinheiro:** R$ 256,3 milhões de R$ 320,7 milhões (79,9%).
- **Por cargo**, deputado federal recebeu mais (R$ 128,0 milhões), mas o fundão pesa mais na campanha para governador (84,7% do dinheiro do cargo).
- **Por partido**, o PL lidera (R$ 53,0 milhões), seguido de PT, PP, PSD e PDT.
- **Por gênero**, candidatas receberam 35,5% do fundão e candidatos, 64,5%.
- **Qualidade dos dados:** há 79 receitas sem data (marcadas com o texto `#NULO`), receitas com datas fora do período da campanha e linhas repetidas (226 na base completa, 386 no recorte do fundão, somando R$ 1,85 milhão). Os totais estão levemente inflados, e a limpeza fica para o próximo projeto.

## Dados

- **Fonte:** Portal de Dados Abertos do TSE, "Prestação de Contas Eleitorais 2026", recurso "Prestação de contas de candidatos".
- **Download:** https://cdn.tse.jus.br/estatistica/sead/odsele/prestacao_contas/prestacao_de_contas_eleitorais_candidatos_2026.zip
- **Arquivo usado:** `receitas_candidatos_2026_RS.csv` (separador `;`, codificação latin-1).
- **Dicionário das colunas:** `leiame_receitas-candidatos.pdf`, dentro do zip.

Os dados **não estão no repositório**, por causa do tamanho. Baixe o zip, extraia e coloque o CSV na pasta `data/`. Como a análise é feita em código, basta baixar um arquivo mais novo e rodar os notebooks de novo para atualizar os números.

## Estrutura

```
fundao-eleitoral/
├── data/          ← dados do TSE (fora do Git)
├── notebooks/
│   ├── exploracao.ipynb   ← primeira leitura da base
│   ├── 01_nivel1.ipynb    ← exercícios 1 a 6
│   ├── 02_nivel2.ipynb    ← exercícios 7 a 11
│   └── 03_nivel3.ipynb    ← exercícios 12 a 15
├── pyproject.toml
└── uv.lock
```

## Como rodar

```bash
git clone https://github.com/RafaelsBahr/fundao-eleitoral.git
cd fundao-eleitoral
uv sync
```

Coloque o CSV em `data/`, abra os notebooks no VS Code e selecione o kernel `.venv`.

## Ferramentas

Python, pandas, Jupyter Notebook, uv, Git e GitHub.

## Autor

Rafael Sedrez Bahr: [github.com/RafaelsBahr](https://github.com/RafaelsBahr)