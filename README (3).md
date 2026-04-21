# Tutorial: Weights & Biases (W&B)

Tutorial prático em Jupyter Notebook para configuração e uso do Weights & Biases em projetos de Machine Learning.

O W&B é uma plataforma de rastreamento de experimentos que registra hiperparâmetros, métricas de treinamento e resultados de forma centralizada, permitindo comparação entre execuções e reprodutibilidade.

## Conteúdo

O notebook cobre o ciclo completo de treinamento de um Perceptron Multicamada (`MLPClassifier`) no dataset de dígitos do scikit-learn, com foco na integração com o W&B:

| Etapa | Função | O que faz |
|-------|--------|-----------|
| 1 | `wandb.init()` | Abre uma run de monitoramento |
| 2 | `config` | Registra hiperparâmetros (learning rate, epochs, batch size) |
| 3 | `wandb.log()` | Envia métricas (loss, accuracy) a cada época |
| 4 | `wandb.summary` | Registra métricas finais para comparação entre runs |
| 5 | `wandb.Table` | Loga dados tabulares (predições individuais) |

## Pré-requisitos

- Python 3.8+
- Conta gratuita no [Weights & Biases](https://wandb.ai)

## Instalação

```bash
git clone https://github.com/maradantaspereira-eng/tutorial-wandb.git
cd tutorial-wandb
```

```bash
pip install wandb scikit-learn numpy jupyter
```

Autentique-se no W&B (obtenha sua API key em [wandb.ai/authorize](https://wandb.ai/authorize)):

```bash
wandb login
```

## Execução

Abra o notebook no VS Code ou Jupyter:

```bash
jupyter notebook tutorial_wandb.ipynb
```

Execute as células na ordem. Cada seção contém explicações em Markdown seguidas do código correspondente.

Após rodar a primeira célula de código, o W&B imprime um link no output. Acesse esse link para acompanhar as métricas em tempo real no painel.

## Estrutura do repositório

```
tutorial-wandb/
    README.md
    tutorial_wandb.ipynb
```

## Tecnologias

- Python
- Jupyter Notebook
- scikit-learn
- Weights & Biases

## Referências

- [Documentação W&B](https://docs.wandb.ai)
- [wandb.init()](https://docs.wandb.ai/ref/python/init)
- [wandb.log()](https://docs.wandb.ai/ref/python/log)
- [wandb.Table](https://docs.wandb.ai/guides/tables)
