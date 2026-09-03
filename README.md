# Rastreamento de Objetos

Pipeline de Visão Computacional para detecção e rastreamento de objetos em imagens e vídeos utilizando Deep Learning.

## Objetivo

Desenvolver uma solução completa de Visão Computacional capaz de detectar e rastrear objetos em imagens, vídeos e câmera em tempo real.

O projeto será construído como um pipeline reproduzível, abrangendo desde a preparação e validação do dataset até treinamento, avaliação, análise de erros e disponibilização do modelo através de uma API.

## Tecnologias

- Python
- PyTorch
- YOLO
- OpenCV
- NumPy
- Pandas
- Matplotlib
- FastAPI
- Docker
- Pytest
- Ruff
- Git

## Problema

O sistema será treinado para detectar as seguintes classes:

| Classe       | Descrição   |
| ------------ | ----------- |
| `person`     | Pessoa      |
| `car`        | Carro       |
| `motorcycle` | Motocicleta |
| `bus`        | Ônibus      |
| `truck`      | Caminhão    |
| `bicycle`    | Bicicleta   |

## Pipeline

```text
Dataset
   │
   ▼
Data Validation
   │
   ▼
Pre-processing
   │
   ▼
Data Augmentation
   │
   ▼
YOLO / PyTorch
   │
   ▼
Training
   │
   ▼
Evaluation
   │
   ▼
Error Analysis
   │
   ▼
Inference
   │
   ├── Image
   ├── Video
   └── Webcam
   │
   ▼
FastAPI

## Estrutura
rastreamentoObjetos/
│
├── src/
│   ├── data/
│   ├── models/
│   ├── training/
│   ├── inference/
│   └── evaluation/
│
├── scripts/
├── tests/
├── notebooks/
├── configs/
│
├── .gitignore
├── README.md
├── pyproject.toml
└── requirements.txt

## Dataset
O dataset será utilizado para treinamento, validação e teste do modelo.

A documentação incluirá:

origem do dataset
quantidade de imagens
classes
distribuição das classes
divisão entre treino, validação e teste
processo de anotação
validação das anotações
técnicas de augmentation

## Avaliação
O modelo será avaliado utilizando métricas específicas para detecção de objetos:

Precision
Recall
mAP@50
mAP@50:95
IoU
matriz de confusão

Além das métricas, será realizada uma análise qualitativa dos erros.

## Análise de erros
Serão investigados casos como:

falsos positivos
falsos negativos
objetos pequenos
objetos parcialmente ocultos
baixa iluminação
sobreposição entre objetos
baixa confiança
classes com desempenho inferior

## EXPERIMENTOS
Os experimentos serão documentados e comparados de forma reproduzível. Sendo preenchidos após os treinamentos.

| Experimento   | Modelo | Augmentation | Resolução | mAP@50 |
| ------------- | ------ | ------------ | --------- | ------ |
| Baseline      | YOLO   | Não          | -         | -      |
| Experiment 01 | YOLO   | Sim          | -         | -      |
| Experiment 02 | YOLO   | Sim          | -         | -      |


## Inferência

Imagem:
python scripts/predict.py --source image.jpg

Vídeo:
python scripts/predict.py --source video.mp4

Webcam:
python scripts/predict.py --source 0

## Reprodutibilidade
O projeto será estruturado para permitir que os experimentos sejam reproduzidos através de:

configuração centralizada
controle de versões
seeds
registro de experimentos
dependências documentadas
Docker

## Roadmap
 Definição do projeto
 Estrutura inicial
 Configuração do Python
 Dependências
 Configuração do ambiente virtual
 Escolha do dataset
 Download e organização dos dados
 Validação do dataset
 Pré-processamento
 Data augmentation
 Treinamento do modelo
 Avaliação
 Análise de erros
 Inferência em imagens
 Inferência em vídeos
 Tracking de objetos
 API FastAPI
 Interface web
 Docker
 Testes automatizados
 CI/CD
 Documentação final
```
