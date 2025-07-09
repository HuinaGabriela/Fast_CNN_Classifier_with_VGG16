## Sobre o Projeto

Este projeto treina um modelo de inteligência artificial para classificar imagens com poucas amostras, usando um modelo pronto como base. É uma forma eficiente de ensinar a máquina a reconhecer imagens sem começar do zero.

O projeto demonstra o uso de transferência de aprendizado para construir um classificador de imagens eficiente a partir de um conjunto de dados relativamente pequeno. Utilizamos o modelo pré-treinado VGG16, removendo sua camada de saída original e adicionando um novo módulo de classificação para as classes específicas do problema.

As camadas convolucionais do modelo base são congeladas inicialmente para extrair características, enquanto treinamos o novo classificador. Em seguida, aplicamos ajuste fino (fine-tuning) nas últimas camadas para aprimorar a precisão do modelo.

O desenvolvimento foi realizado com as bibliotecas TensorFlow e Keras, utilizando o ambiente colaborativo do Google Colab para acelerar o treinamento. Os dados foram gerenciados e disponibilizados via Kaggle, facilitando o acesso e a organização do conjunto de imagens.

Ao final, o modelo treinado é avaliado, validado e salvo para futuras inferências.


# 📊 Criação de Dataset para Treinamento de Redes Neurais (dataset concluido)

Este repositório faz parte das atividades do **Bootcamp de Machine Learning** e tem como objetivo primeiramente a **criação de um dataset personalizado**, que será utilizado ao longo da trilha em diferentes projetos de aprendizado de máquina.

## 🧠 Atividade Proposta

Criar uma **base de dados (dataset)** para o treinamento de um algoritmo de **Inteligência Artificial baseado em Redes Neurais Artificiais (RNA)**.

### Requisitos:

- Criar pelo menos duas classe distintas.
- Cada classe deve conter no mínimo 100 imagens.
- As imagens podem ser:
  - Capturadas por câmera (ex: celular)
  - Baixadas da internet
- As imagens devem ter qualidade mínima de 400x400 pixels.
- Exemplo utilizado neste projeto: 
  - Classe 1: gatos 🐱
  - Classe 2: cachorros 🐶

🗂 Estrutura Esperada do Dataset
```
dataset/
├── classe_1/
│   ├── imagem1.jpg
│   ├── imagem2.jpg
│   └── ...
├── classe_2/
│   ├── imagem1.jpg
│   ├── imagem2.jpg
│   └── ...
```
---

## 📘 Diagrama de Atividades
```
[Início]
  |
  v
[Carregar e preparar conjunto de dados de imagens]
  |
  v
[Importar modelo VGG16 sem a camada de classificação final]
  |
  v
[Acoplar um novo módulo de classificação ao modelo base]
  |
  v
[Congelar as camadas convolucionais do modelo base]
  |
  v
[Compilar o modelo]
  |
  v
[Treinar somente o novo módulo de classificação]
  |
  v
[Descongelar as últimas camadas do modelo base (opcional)]
  |
  v
[Realizar ajuste fino]
  |
  v
[Avaliar desempenho final]
  |
  v
[Salvar modelo treinado]
  |
  v
[Fim]
```
📝 Explicações rápidas dos termos técnicos:

Modelo base (backbone): Parte da rede pré-treinada (como VGG16) usada para extração de características.

Módulo de classificação: Novo conjunto de camadas adicionadas para adaptar o modelo à nova tarefa.

Congelar: Impedir que os pesos sejam atualizados durante o treinamento.

Ajuste fino (fine-tuning): Treinar algumas camadas do modelo base com taxa de aprendizado pequena para adaptar à nova tarefa.

---

## 📌 Links Úteis

- https://www.tensorflow.org/datasets/catalog/cats_vs_dogs?hl=pt-br
- https://colab.research.google.com/github/kylemath/ml4a-guides/blob/master/notebooks/transfer-learning.ipynb#scrollTo=VWWN-FPLYoZs

📘 **Introdução para à Computação Bioinspirada:**
- https://homepages.dcc.ufmg.br/~glpappa/cverao/CursoVerao-Parte1.pdf  
- https://www.inf.ufpr.br/aurora/disciplinas/topicosia2/aulas/aula1.pdf  
- https://edisciplinas.usp.br/pluginfile.php/4256863/mod_resource/content/1/cb_3_ce_ag_1.pdf  

🧬 **Algoritmos Genéticos:**
- https://www.inf.ufsc.br/~mauro.roisenberg/ine5377/Cursos-ICA/CE-intro_apost.pdf  

🧠 **Redes Neurais Artificiais:**
- https://www.inf.ufsc.br/~j.barreto/tutoriais/Survey.pdf
