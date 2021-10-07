# Django_Documenta-o
Aprender django pela documentação oficial

# criar env
python -m venv env
	-- cmd --
.\env\Scripts\activate.bat
	-- powerScript--
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
.\env\Scripts\activate.sp1

# Instalar Django
python -m pip install Django

# Versão
python -m django --version

# Criando um projeto
django-admin startproject mysite

**
	-> O diretório mysite/ exterior é um contêiner para o seu projeto. Seu nome não importa para o Django; você pode renomeá-lo para qualquer nome que você quiser.
	-> manage.py: um utilitário de linha de comando que permite a você interagir com esse projeto Django de várias maneiras. Você pode ler todos os detalhes sobre o manage.py em django-admin and manage.py.
	-> O diretório mysite/ interior é o pacote Python para o seu projeto. Seu nome é o nome do pacote Python que você vai precisar usar para importar coisas do seu interior (por exemplo, mysite.urls).
	-> mysite/__init__.py: um arquivo vazio que diz ao Python que este diretório deve ser considerado um pacote Python. Se você é um iniciante Python, leia mais sobre pacotes na documentação oficial do Python.
	-> mysite/settings.py: configurações para este projeto Django. Configurações do Django irá revelar para você tudo sobre o funcionamento do settings.
	-> mysite/urls.py: as declarações de URLs para este projeto Django; um “índice” de seu site movido a Django. Você pode ler mais sobre URLs em Despachante de URL.
	-> mysite/asgi.py: um ponto de integração para servidores web compatíveis com ASGI usado para servir seu projeto. Veja Como fazer o deploy com ASGI para mais detalhes.
	-> mysite/wsgi.py: um ponto de integração para servidores web compatíveis com WSGI usado para servir seu projeto. Veja Como implementar com WSGI para mais detalhes.
**

# O servidor de desenvolvimento
python manage.py runserver

# Criando a aplicação de enquetes: Polls
python manage.py startapp polls

# Criar Tabela no banco de dados
python manage.py migrate

# Quando realizar mudanças em models
python manage.py makemigrations polls

Mude seus modelos (em models.py).
Rode python manage.py makemigrations para criar migrações para suas modificações
Rode python manage.py migrate para aplicar suas modificações no banco de dados.



# Criar usuario para acessar o banco
python manage.py createsuperuser