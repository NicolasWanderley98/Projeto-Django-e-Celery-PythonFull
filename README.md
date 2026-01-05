Este repositório é para a fixação dos conhecimentos obtidos no curso pythonando contém um projeto Django integrado com Celery para processamento de tarefas assíncronas em Python.

O Celery é uma fila de tarefas distribuída que permite executar trabalhos em segundo plano (como envio de e-mails, processamento de arquivos ou qualquer operação demorada) separadamente do ciclo de requisição/response do Django — mantendo a aplicação responsiva e escalável. 
GitHub

🧠 Funcionalidades

✅ Estrutura de projeto Django
✅ Integração com Celery para tarefas assíncronas
✅ Tarefas configuradas para execução em background
✅ Gerenciamento de workers Celery
(Adicione aqui outras funcionalidades específicas do seu projeto)

🚀 Tecnologias Utilizadas
Ferramenta	Versão / Descrição
Python	3.x
Django	Framework web Python
Celery	Fila de tarefas assíncronas em Python (integrado ao Django) 
GitHub

Redis / RabbitMQ	(Opcional: broker de mensagens para Celery)

💡 Ajuste esta tabela conforme as versões e tecnologias que você usa no projeto.

📌 Pré-Requisitos

Antes de começar, você precisa ter instalado:

Python 3.x

Pip (ou Poetry/Poetry)

Broker de mensagens (ex.: Redis ou RabbitMQ) para o Celery
(adicione aqui outros requisitos que o projeto exige)

🛠️ Instalação

Clone o repositório:

git clone https://github.com/NicolasWanderley98/Projeto-Django-e-Celery-PythonFull.git
cd Projeto-Django-e-Celery-PythonFull


Crie e ative o ambiente virtual:

python3 -m venv .venv
source .venv/bin/activate


Instale as dependências:

pip install -r requirements.txt


Configure as variáveis de ambiente (se aplicável):

DJANGO_SECRET_KEY="sua_chave_aqui"
BROKER_URL="redis://localhost:6379/0"


Rode as migrações:

python manage.py migrate

▶️ Executando o Projeto
🧩 Iniciar o servidor Django:
python manage.py runserver

🔄 Iniciar o Celery Worker:
celery -A projeto_celery worker --loglevel=info


Substitua projeto_celery pelo nome do seu módulo Celery, se for diferente.

🧪 Testando Tarefas Celery

📍 Certifique-se de que o broker (ex.: Redis) está rodando antes de executar tarefas.

Você pode testar uma tarefa Celery chamada de forma assíncrona assim:

from app.tasks import minha_tarefa

minha_tarefa.delay(param1, param2)

📁 Estrutura do Projeto

Projeto-Django-e-Celery-PythonFull/

├── .gitignore

├── manage.py

├── projeto_celery/         # Django + Celery configs

├── app/                    # Seus apps Django

├── requirements.txt

└── README.md


Exemplos de estrutura — ajuste de acordo com o seu projeto real.
