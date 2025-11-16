# 🧠 Engenharia_SoftwareII_2025-2_T04_crawl4ai

### Projeto de Análise Arquitetural com Modelos de Linguagem (LLMs)

**Disciplina:** Engenharia de Software II – UFS  
**Turma:** 2025/2 – T04  
**Equipe:** Adriel Menezes Santana - 202100022659
Luan Feitosa Lima Sátiro - 202300061714
Luan Prata Mendonça - 202000138885
Paulo Henrique Carvalho de Andrade - 202200060090
Paulo Henrique dos Santos Reis - 202100115524
Thiago Mecena Silva - 202100045840
Victoria Moura Santos - 202000138900

---

## 🚀 Execução no Google Colab

No GitHub, clique no botão
“Open in Colab”:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/luan-feitosa/Engenharia_SoftwareII_2025-2_T04_crawl4ai/blob/main/main.ipynb)

(ou use o link direto abaixo):

```bash
https://colab.research.google.com/github/luan-feitosa/Engenharia_SoftwareII_2025-2_T04_crawl4ai/blob/main/main.ipynb
```

---

## 🔍 Visão Geral

Este projeto tem como objetivo aplicar **Modelos de Linguagem (LLMs)** para **analisar a arquitetura de software** de repositórios no GitHub, identificando padrões arquiteturais, design patterns e características estruturais (módulos, camadas, dependências, etc).

Além disso, o notebook compara os resultados obtidos em cada passo e gera um relatorio final comparando os padrões encontrados.

---

## 🧰 Tecnologias Utilizadas

-   **Python 3.x**
-   **Google Colab** (execução online, sem instalação local)
-   **Bibliotecas:**
    -   `sentence_transformers`
    -   `requests`, `os`, `json`, `shutil`
    -   `numpy`
    -   `openai`
    -   `sklearn.cluster`
    -   `radon`

---

💻 Infraestrutura de Análise

Toda a metodologia de pipeline e a execução dos três modelos de linguagem foram realizadas na plataforma Google Colab. Utilizamos o ambiente de execução gratuito, que fornece acesso a GPUs NVIDIA T4 (ou similares, dependendo da disponibilidade no momento da execução). Esta infraestrutura foi suficiente para carregar e executar todos os modelos de análise (Llama 3.1 8B, DeepSeek V3.2 Exp e Qwen 2.5 7B), permitindo que todo o pipeline de 6 etapas fosse concluído para cada modelo.

---

## 💻 Como Executar (Metodologia de Comparação)

1.  Abra o link do Google Colab.
2.  Instale as dependências (primeira célula `!pip install...`).
3.  Coloque sua chave de API do Hugging Face na Célula 2.

**Para comparar os 3 Modelos:**

O notebook deve ser executado **três vezes**, uma para cada modelo.

4.  Na **Célula 2**, localize a variável `MODELO_HF`.
5.  Escolha um dos três modelos que analisamos:
    * `MODELO_HF = "meta-llama/Llama-3.1-8B-Instruct"`
    * `MODELO_HF = "deepseek-ai/DeepSeek-V3.2-Exp"`
    * `MODELO_HF = "Qwen/Qwen2.5-7B-Instruct"`
6.  Execute todas as células em sequência (no menu, "Ambiente de execução" > "Executar tudo").
7.  Salve o relatório final gerado.
8.  Repita os passos 5 a 7 para os outros dois modelos.

**Justificativa dos Modelos:**
[cite_start]Selecionamos estes três modelos (Llama 3.1, DeepSeek V3.2, e Qwen 2.5) [cite: 634-636] por serem modelos de chat (Instruct) de tamanho similar (aprox. 7-8B de parâmetros) e de alta performance, permitindo uma comparação justa sobre como diferentes arquiteturas de LLM interpretam e analisam o código-fonte.

OBS: lembre de baixar o arquivo final e/ou salva-lo com um nome diferente pois quando rodar novamente com outra LLM o arquivo.md sera sobrescrito.

---

📊 Saídas Geradas

-   relatorios_passos.md → Relatórios Markdown contendo:
    -   Padrões arquiteturais detectados
-   relatorio_final.md:
    -   Comparação entre resultados de cada passo.

(Arquivos salvos no diretório atual do Colab ou no seu Drive, se montado.)

---

✅ Funcionalidades Principais

-   📂 Clonagem local de repositórios GitHub (sem usar API externa).
-   🧩 Identificação de padrões arquiteturais e design patterns.
-   📄 Geração automática de relatório em Markdown com o resultado da LLM usada.
