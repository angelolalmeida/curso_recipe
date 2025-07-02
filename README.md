# 🍳 Projeto Receitas - Django

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Django](https://img.shields.io/badge/Django-4.2+-green.svg)](https://www.djangoproject.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Projeto de estudo desenvolvido durante o curso de Django Web Framework**  
> 📚 Baseado no curso: [Curso de Django Web Framework com Python, HTML e CSS](https://www.udemy.com/course/curso-de-django-web-framework-com-python-html-e-css/)

## 🎯 Sobre o Projeto

Este é um projeto de estudo focado no desenvolvimento web com Django, criado para aprender e praticar os conceitos fundamentais do framework. O projeto simula uma aplicação de receitas culinárias, permitindo aos usuários visualizar, criar e gerenciar receitas.

### ✨ Funcionalidades Principais

- 📖 **Listagem de Receitas** - Visualize todas as receitas disponíveis
- 🔍 **Detalhes da Receita** - Veja informações completas de cada receita
- ➕ **Criação de Receitas** - Adicione novas receitas ao sistema
- ✏️ **Edição de Receitas** - Modifique receitas existentes
- 🗑️ **Exclusão de Receitas** - Remova receitas do sistema
- 👤 **Sistema de Usuários** - Autenticação e autorização
- 🎨 **Interface Responsiva** - Design adaptável para diferentes dispositivos

## 🛠️ Tecnologias Utilizadas

### Backend
- **Python 3.12+** - Linguagem principal
- **Django 4.2+** - Framework web
- **SQLite** - Banco de dados (desenvolvimento)
- **Django Admin** - Interface administrativa

### Frontend
- **HTML5** - Estrutura das páginas
- **CSS3** - Estilização e layout
- **JavaScript** - Interatividade
- **Bootstrap** - Framework CSS
- **FontAwsome 6.6** - Ícones (usei o pacote do próprio Django)

### Ferramentas de Desenvolvimento
- **VS Code** - Editor de código
- **Git** - Controle de versão
- **Virtual Environment** - Isolamento de dependências

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Python 3.12 ou superior
- pip (gerenciador de pacotes Python)
- Git

### 1. Clone o Repositório

```bash
git clone https://github.com/angelolalmeida/curso_recipe.git
cd curso_recipe
```

### 2. Configure o Ambiente Virtual

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

### 3. Instale as Dependências

```bash
pip install -r requirements.txt
```

### 4. Configure as Variáveis de Ambiente

```bash
# Copie o arquivo de exemplo
cp env_template.txt .env

# Edite o arquivo .env com suas configurações
```

### 5. Execute as Migrações

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Crie um Superusuário (Opcional)

```bash
python manage.py createsuperuser
```

### 7. Execute o Servidor

```bash
python manage.py runserver
```

### 8. Acesse a Aplicação

- **Aplicação**: http://localhost:8000
- **Admin**: http://localhost:8000/admin

## 📁 Estrutura do Projeto

```
curso_recipe/
├── recipe_course/          # Configurações principais do Django
│   ├── settings.py        # Configurações do projeto
│   ├── urls.py           # URLs principais
│   └── wsgi.py           # Configuração WSGI
├── recipes/              # App principal de receitas
│   ├── models.py         # Modelos de dados
│   ├── views.py          # Lógica de negócio
│   ├── urls.py           # URLs do app
│   ├── admin.py          # Configuração do admin
│   └── templates/        # Templates HTML
├── templates/            # Templates globais
├── static/              # Arquivos estáticos (CSS, JS, imagens)
├── media/               # Arquivos de mídia enviados pelos usuários
├── manage.py            # Script de gerenciamento do Django
├── requirements.txt     # Dependências do projeto
└── README.md           # Este arquivo
```

## 🎓 O que Aprendi

### Conceitos do Django
- ✅ **MVT (Model-View-Template)** - Arquitetura do Django
- ✅ **URLs e Roteamento** - Mapeamento de URLs para views
- ✅ **Models e Migrations** - Modelagem de dados
- ✅ **Forms** - Processamento de formulários
- ✅ **Templates e Template Tags** - Renderização de HTML
- ✅ **Static Files** - Gerenciamento de arquivos estáticos
- ✅ **Django Admin** - Interface administrativa

### Boas Práticas
- ✅ **Estrutura de Projeto** - Organização de código
- ✅ **Ambiente Virtual** - Isolamento de dependências
- ✅ **Versionamento** - Controle com Git
- ✅ **Documentação** - README e comentários
- ✅ **Configuração** - Variáveis de ambiente

## 📚 Recursos de Aprendizado

### Curso Base
- **Curso**: [Curso de Django Web Framework com Python, HTML e CSS](https://www.udemy.com/course/curso-de-django-web-framework-com-python-html-e-css/)
- **Instrutor**: Luiz Otávio Miranda
- **Plataforma**: Udemy

### Documentação Oficial
- [Django Documentation](https://docs.djangoproject.com/)
- [Django Tutorial](https://docs.djangoproject.com/en/stable/intro/tutorial01/)

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👨‍💻 Autor

**Angelo Almeida**
- GitHub: [@angelolalmeida](https://github.com/angelolalmeida)
- LinkedIn: [https://www.linkedin.com/in/angelo-almeida-cientista-dados/](https://www.linkedin.com/in/angelo-almeida-cientista-dados/)

## 🙏 Agradecimentos

- Ao instrutor do curso Luiz Otávio, é o segundo curso dele que eu faço e eu gosto muito da didática dele. OBS: assista o curso no 2x.
- À comunidade Django por criar um framework incrível


---

⭐ **Se este projeto te ajudou, considere dar uma estrela!**

---

*Desenvolvido com ❤️ durante o aprendizado de Django*
