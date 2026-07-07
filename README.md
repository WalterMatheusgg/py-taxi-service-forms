# Taxi Service Forms

## Descrição

O **Taxi Service Forms** é uma aplicação web desenvolvida com **Django** para praticar o uso de formulários, operações CRUD e views baseadas em classes.

O sistema simula uma plataforma de gerenciamento de serviço de táxi, permitindo administrar carros, fabricantes e motoristas. Esta versão do projeto tem como foco principal a criação, atualização e exclusão de registros utilizando Django Forms e Class-Based Views.

## Funcionalidades

- Listagem de carros, fabricantes e motoristas;
- Visualização de detalhes de carros e motoristas;
- Criação, edição e exclusão de carros;
- Criação, edição e exclusão de fabricantes;
- Uso de formulários do Django;
- Proteção de páginas com autenticação;
- Paginação nas listas;
- Organização das rotas, views, models e templates;
- Otimização de consultas com `select_related` e `prefetch_related`.

## Tecnologias utilizadas

- Python
- Django
- SQLite
- HTML
- CSS
- Django Templates
- Django Crispy Forms
- Git
- GitHub

## Estrutura do projeto

```text
py-taxi-service-forms/
├── taxi/
│   ├── migrations/
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
├── taxi_service/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
├── templates/
├── static/
├── manage.py
├── requirements.txt
└── README.md
```

## Modelos principais

### Manufacturer

Representa uma fabricante de carros.

Principais campos:

- `name`: nome da fabricante;
- `country`: país de origem.

### Driver

Representa um motorista do serviço de táxi.

Principais campos:

- `username`: nome de usuário;
- `first_name`: primeiro nome;
- `last_name`: sobrenome;
- `license_number`: número da licença.

### Car

Representa um carro utilizado no serviço de táxi.

Principais campos:

- `model`: modelo do carro;
- `manufacturer`: fabricante do carro;
- `drivers`: motoristas associados ao carro.

## O que foi praticado

Este projeto permitiu praticar conceitos importantes do Django, como:

- Criação de operações CRUD;
- Uso de Class-Based Views;
- Criação e renderização de formulários;
- Relacionamento entre models;
- Proteção de views com autenticação;
- Organização de templates e URLs;
- Paginação;
- Boas práticas de estruturação em projetos Django.

## Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/WalterMatheusgg/py-taxi-service-forms.git
```

### 2. Acesse a pasta do projeto

```bash
cd py-taxi-service-forms
```

### 3. Crie um ambiente virtual

```bash
python -m venv venv
```

### 4. Ative o ambiente virtual

No Windows:

```bash
venv\Scripts\activate
```

No Linux/macOS:

```bash
source venv/bin/activate
```

### 5. Instale as dependências

```bash
pip install -r requirements.txt
```

### 6. Execute as migrações

```bash
python manage.py migrate
```

### 7. Carregue os dados iniciais

```bash
python manage.py loaddata taxi_service_db_data.json
```

### 8. Inicie o servidor

```bash
python manage.py runserver
```

Depois, acesse no navegador:

```text
http://127.0.0.1:8000/
```

## Usuário padrão

Após carregar os dados iniciais, é possível acessar com:

```text
Username: admin.user
Password: 1qazcde3
```

## Autor

Desenvolvido por **Walter Matheus** como parte da trilha de estudos em Django.
