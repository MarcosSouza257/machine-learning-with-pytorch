# Machine Learning with PyTorch — Udacity

Repositório com os projetos desenvolvidos durante o nanodegree **[Intro to Machine Learning with PyTorch](https://www.udacity.com/course/intro-to-machine-learning-nanodegree--nd229)** da Udacity.

## Projetos

| # | Projeto | Descrição | Técnicas |
|---|---------|-----------|----------|
| 1 | [Finding Donors for CharityML](project_1/) | Previsão de renda com dados do censo americano para identificar potenciais doadores | Aprendizado supervisionado |
| 2 | [CIFAR-10 Image Classifier](project_2/CIFAR-10_Image_Classifier-STARTER.ipynb) | Classificação de imagens em dez categorias do conjunto CIFAR-10 | CNN, data augmentation, batch normalization e dropout |

## Project 2 — CIFAR-10 Image Classifier

O segundo projeto implementa uma rede neural convolucional em PyTorch para classificar as dez categorias do CIFAR-10. O modelo utiliza três blocos convolucionais com 32, 64 e 128 canais, seguidos por uma camada totalmente conectada e uma saída `Softmax` com dez probabilidades.

O treinamento foi realizado durante 25 épocas com `AdamW`, `NLLLoss`, normalização, recorte aleatório e espelhamento horizontal. O modelo treinado alcançou os seguintes resultados no conjunto de teste:

| Métrica | Resultado |
|---------|-----------|
| Acurácia | **85,27%** |
| Previsões corretas | 8.527 de 10.000 |
| Test loss | 0,4500 |
| Meta do projeto | 70% |

### Artefatos

- [Notebook completo](project_2/CIFAR-10_Image_Classifier-STARTER.ipynb)
- [Checkpoint do modelo treinado](project_2/CIFAR10_model_checkpoint.pth)

O CIFAR-10 é baixado automaticamente pelo `torchvision` durante a execução. Os arquivos locais do dataset são armazenados em `project_2/images/` e não são versionados no repositório.

## Tecnologias

- Python 3.x e Jupyter Notebook
- NumPy, Pandas e Matplotlib
- scikit-learn
- PyTorch e torchvision

## Como executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/marcosquant/machine-learning-with-pytorch.git
   cd machine-learning-with-pytorch
   ```

2. Crie um ambiente virtual e instale as dependências:

   ```bash
   python -m venv .venv
   # Windows PowerShell: .venv\Scripts\Activate.ps1
   # Linux/macOS: source .venv/bin/activate
   pip install numpy pandas matplotlib scikit-learn torch torchvision jupyter
   ```

3. Inicie o Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Abra o notebook desejado:

   - `project_1/finding_donors.ipynb`
   - `project_2/CIFAR-10_Image_Classifier-STARTER.ipynb`

O treinamento do Project 2 utiliza CUDA automaticamente quando uma GPU compatível está disponível, mas também pode ser executado em CPU.

## Autor

**Marcos Roberto Souza** — nanodegree [Intro to Machine Learning with PyTorch](https://www.udacity.com/course/intro-to-machine-learning-nanodegree--nd229), Udacity.
