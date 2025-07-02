# Configuração de Variáveis de Ambiente para Django 4.2

Este projeto está configurado para usar variáveis de ambiente seguindo as melhores práticas de segurança.

## 📋 Pré-requisitos

- Python 3.8+
- Django 4.2 LTS
- pip

## 🚀 Instalação

### 1. Instalar dependências
```bash
pip install -r requirements.txt
```

### 2. Criar arquivo .env
Copie o template e renomeie para `.env`:
```bash
cp env_template.txt .env
```

### 3. Configurar variáveis de ambiente
Edite o arquivo `.env` com suas configurações:

```bash
# Configurações básicas
DEBUG=True
SECRET_KEY=sua-chave-secreta-aqui
ALLOWED_HOSTS=localhost,127.0.0.1

# Banco de dados
DATABASE_URL=sqlite:///db.sqlite3

# Email (opcional)
EMAIL_HOST_USER=seu-email@gmail.com
EMAIL_HOST_PASSWORD=sua-senha-de-app
```

## 🔐 Geração de SECRET_KEY

Para gerar uma SECRET_KEY segura:

```python
from django.core.management.utils import get_random_secret_key
print(get_random_secret_key())
```

Ou use o comando:
```bash
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```

## 📁 Estrutura de Arquivos

```
projeto/
├── .env                    # Variáveis de ambiente (NÃO versionado)
├── .gitignore             # Ignora .env e outros arquivos sensíveis
├── env_template.txt       # Template das variáveis de ambiente
├── requirements.txt       # Dependências do projeto
├── django_env_settings.py # Configurações Django com variáveis de ambiente
└── README_ENV_SETUP.md    # Este arquivo
```

## 🔧 Configurações por Ambiente

### Desenvolvimento
```bash
DEBUG=True
SECURE_SSL_REDIRECT=False
SESSION_COOKIE_SECURE=False
CSRF_COOKIE_SECURE=False
```

### Produção
```bash
DEBUG=False
SECURE_SSL_REDIRECT=True
SESSION_COOKIE_SECURE=True
CSRF_COOKIE_SECURE=True
SECURE_HSTS_SECONDS=31536000
```

## 🗄️ Configuração de Banco de Dados

### SQLite (desenvolvimento)
```bash
DATABASE_URL=sqlite:///db.sqlite3
```

### PostgreSQL (produção)
```bash
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
```

### MySQL
```bash
DATABASE_URL=mysql://user:password@localhost:3306/dbname
```

## 📧 Configuração de Email

### Gmail
```bash
EMAIL_BACKEND=django.core.mail.backends.smtp.EmailBackend
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True
EMAIL_HOST_USER=seu-email@gmail.com
EMAIL_HOST_PASSWORD=sua-senha-de-app
```

### Console (desenvolvimento)
```bash
EMAIL_BACKEND=django.core.mail.backends.console.EmailBackend
```

## 🔒 Configurações de Segurança

### Configurações recomendadas para produção:
```bash
SECURE_BROWSER_XSS_FILTER=True
SECURE_CONTENT_TYPE_NOSNIFF=True
SECURE_HSTS_SECONDS=31536000
SECURE_HSTS_INCLUDE_SUBDOMAINS=True
SECURE_HSTS_PRELOAD=True
SECURE_SSL_REDIRECT=True
SESSION_COOKIE_SECURE=True
CSRF_COOKIE_SECURE=True
```

## 🚀 Deploy

### Heroku
```bash
# Configurar variáveis no Heroku
heroku config:set SECRET_KEY=sua-chave-secreta
heroku config:set DEBUG=False
heroku config:set DATABASE_URL=postgresql://...
```

### Vercel
Crie um arquivo `vercel.json`:
```json
{
  "env": {
    "SECRET_KEY": "sua-chave-secreta",
    "DEBUG": "False",
    "DATABASE_URL": "postgresql://..."
  }
}
```

## 📝 Logs

Os logs são salvos em `logs/django.log` por padrão. Configure no `.env`:

```bash
LOG_LEVEL=INFO
LOG_FILE=logs/django.log
```

## 🔍 Debug

Para desenvolvimento, você pode usar:
```bash
DEBUG=True
```

Isso ativa:
- Páginas de erro detalhadas
- Debug toolbar
- Logs verbosos

## ⚠️ Importante

1. **NUNCA** commite o arquivo `.env` no Git
2. **SEMPRE** use SECRET_KEYs únicas para cada ambiente
3. **NUNCA** use DEBUG=True em produção
4. **SEMPRE** configure ALLOWED_HOSTS corretamente
5. **SEMPRE** use HTTPS em produção

## 🆘 Solução de Problemas

### Erro: "SECRET_KEY not set"
```bash
# Gere uma nova SECRET_KEY
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```

### Erro: "ALLOWED_HOSTS not set"
```bash
# Adicione seu domínio ao .env
ALLOWED_HOSTS=localhost,127.0.0.1,seudominio.com
```

### Erro: "Database connection failed"
Verifique se a DATABASE_URL está correta no `.env`.

## 📚 Recursos Adicionais

- [Django Documentation](https://docs.djangoproject.com/)
- [Django Security](https://docs.djangoproject.com/en/4.2/topics/security/)
- [python-dotenv](https://github.com/theskumar/python-dotenv)
- [dj-database-url](https://github.com/jacobian/dj-database-url) 