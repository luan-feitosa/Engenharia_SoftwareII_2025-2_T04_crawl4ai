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

## 💻 Como Executar

1. Abra o link acima no **Colab**.
2. (Opcional) Monte seu **Google Drive**:
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
3. Instale as dependências executando a célula inicial do notebook:
    ```bash
    !pip install openai huggingface_hub sentence-transformers scikit-learn numpy
    !pip install radon
    ```
4. Coloque sua chave de API do Hugging Face na celula 2:
    ```python
    if HF_API_KEY == "SUA_API_KEY_AQUI":
    ```
5. Execute todas as células em sequência.
6. O notebook irá:
    - Clonar o repositório a ser analisado;
    - Aplicar LLMs da Hugging Face para detectar padrões arquiteturais;
    - Gerar um relatório final .md.

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
