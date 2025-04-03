# IASA NLP Course

# Setup Working Environment  

## Pre-requirements 

- conda 4.12.0 (later versions may also work) - [Installation](https://docs.anaconda.com/anaconda/install/index.html)
- VS Code - [Ubuntu Installation](https://code.visualstudio.com/docs/setup/linux)
- (Optional) CUDA Version: 11.4; Driver Version: 470.129.06 - [Installation](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html)

## Setup environment 

### Poetry (Recommended)

1. Install Poetry using [Poetry full guide](https://python-poetry.org/docs/#installation).
    - Important: Check if it is working using `poetry --version`
2. Run command to keep your `.venv` folder right in your project: `poetry config virtualenvs.in-project true`
3. `poetry shell`
    - Important: If you have `conda` and 2 environments were activated: `conda deactivate`
4. `poetry install --no-root`

In order to activate environment on the next use. Important: you should be inside your project

`poetry shell`

### Conda

If you have CUDA
```bash
conda env create -f environment_gpu.yaml
```
Otherwise
```bash
conda env create -f environment.yaml
```

In order to activate environment 

```bash
conda activate iasa_nlp_env
```

# Start Jupyter

You may use any port 
```bash
jupyter lab --port 7766
```

# Content 

# NLP та ML: Навчальний Курс

Цей репозиторій містить навчальні матеріали, розділені на чотири модулі.

## Модуль 1: Вступ до NLP / Класичні ML підходи

- **1. Постановка ML задач:**  
  - Структура та структурні елементи постановки ML задачі  
  - Формалізація бізнес задач  
  - Основні задачі й методи в сфері Обробки природних мов

- **2. Представлення мов:**  
  - Представлення природних мов в машинному вигляді  
  - Класичні та нейронні алгоритми векторизації  
  - Класичні ML підходи в NLP

- **3. Оцінка моделей:**  
  - Основні метрики  
  - Побудова оцінки підходів і моделей – валідація (Спільна з аудіо-курсом)

- **4. Основи PyTorch (Спільна з аудіо-курсом)**

  
- **5. Фреймворк Lightnin, Рекурентні нейронні мережі**

## Модуль 2: Глибокі мережі

- **1. Трансформери та енкодери:**  
  - Архітектура трансформер  
  - Використання енкодерів для задачі класифікації на NER

- **2. Кластеризація та тематичне моделювання:**  
  - Задача кластеризації  
  - Задача моделювання тем

- **3. Генеративні задачі:**  
  - Машинний переклад  
  - Сумаризація тексту  
  - Умовна та безумовна текстова генерація

- **4. LLM. Оптимізація ефективності використання: QLoRA, Flash-Attention, KV-Cache**

- **5. LLM. RLHF, DPO finetuning.**

## Модуль 3: RAG (Retrieval Augmented Generation)

- **1. Векторний пошук**

- **2. Retrieval: sparse and dense retrieval, embedding models finetuning**

- **RAG пайплайн:**  
  - Побудова повного RAG пайплайну

## Модуль 4: Операціоналізація NLP рішень

- **Основи MLOps**  

- **Agentic AI**


# Use Kaggle or Colab for computations

## Kaggle 

1. Create [Kaggle](https://www.kaggle.com/) account 
2. Create [Notebook](https://www.kaggle.com/code)
3. Explore [docs](https://www.kaggle.com/docs/notebooks) and find out how 
    - Add Kaggle dataset to notebook 
    - Turn on GPU 

## Colab 

1. Create Notebook in [Colab](https://colab.research.google.com/)
2. Enable GPU 
3. Add Kaggle dataset to Colab - https://www.geeksforgeeks.org/how-to-import-kaggle-datasets-directly-into-google-colab/

# Data

- For most of lectures you will need datasets from Kaggle. [Prepare in advance](#how-to-use-kaggle-datasets)
    - CommonLit - Evaluate Student Summaries dataset API command: `kaggle competitions download -c commonlit-evaluate-student-summaries`
    - Natural Language Processing with Disaster Tweets dataset API command: `kaggle competitions download -c nlp-getting-started`
    - Mantis Analytics Location Detection dataset: `kaggle datasets download -d vladimirsydor/mantis-analytics-location-detection`
    - Dataset for Topic Modelling: `https://drive.google.com/drive/folders/1jwh225T0DIEN4A1wMZ8-dVJX-2Tsovqf?usp=sharing`
- We recommend to create `data` folder in the course root directory and put all datasets there. So you might have next structure

```
data/
    nlp_getting_started/
        train.csv
        test.csv
        ...
    ...
Lecture_1/
...
```

## How to use Kaggle datasets

1. Create [Kaggle](https://www.kaggle.com/) account
2. Proceed [with Installation & Authentication](https://www.kaggle.com/docs/api#getting-started-installation-&-authentication)
3. Don't forget to join a competition and accept its rules on a Kaggle website.
4. Download dataset with API command 

# Feedback [Only For Lectors]

## 2023

Raw table : https://docs.google.com/spreadsheets/d/1P38uhwkMQo0cd1avywbnVJ-dwxiswHpAcIpEHrlv1PY/edit?usp=sharing

# TODO

- [ ] Process recordings and upload them to YouTube
- [ ] Process 2023 Feedback 

# Citation

```
@misc{iasa_nlp_course_2023,
  author = {Sydorskyi Volodymyr, Bazdyrev Anton, Yelisieiev Vladyslav},
  title = {IASA NLP course 2023},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/VSydorskyy/iasa_nlp_course}},
}
```
