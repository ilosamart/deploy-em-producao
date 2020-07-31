# Deploy de aplicação Django (python)

## TODO: Talvez falar um pouco sobre virtualenv antes de entrar no Django

## Introdução

[Django](1) é um *web framework* muito utilizado na comunidade Python, guiado por uma filosofia "pilhas inclusas", o que significa que ele não provê somente o
básico necessário para se criar um produto web, inclui também uma série de ferramentas extras para ajudar no trabalho do desenvolvedor. Veremos aqui que essa 
filosofia auxilia no *deploy* da aplicação e vamos interagir com o *framework* em diversas etapas de nosso *pipeline*.

Antes de entrarmos nas particularidades que envolvem o deploy de uma aplicação Django, vamos relembrar os passos listados no capítulo
**O que deve ter no seu pipeline?**:

1. Build do artefato
1. Teste unitário
1. Provisionamento da infra pré-produção
1. Teste de integração
1. Teste de aceitação
1. Provisionamento de infra produção
1. Deploy de pré-produção
1. Deploy de produção

Abstraindo os passos para provisionamento dos ambientes (que serão semelhantes independentemente da tecnologia da aplicação), vamos focar nas
especificidades do Django e enumerar o que é necessário para executarmos uma aplicação, dividindo esses requisitos em duas partes: python
e Django. Assim, teremos os seguintes requisitos para cada parte:

1. Python
   1. Instalar interpretador Python
   1. Instalar dependências da aplicação (bibliotecas adicionais, por exemplo: django, [cx_Oracle](2) para conectarmos ao Oracle Database)
   1. Instalar bibliotecas nativas do Sistema Operacional (`cx_Oracle` por exemplo requer o *Oracle Instant Client*)
1. Django
   1. Executar migrações de banco de dados (Django possui suporte de fábrica a isso)
   1. Executar coleta de arquivos estáticos do site (Django possui facilidades para gerenciamento de arquivos CSS, JS, imagens)
   1. Instalarmos servidor WSGI (ou ASGI)

Agora, vamos ver em detalhes cada um desses grupos de requisitos.

## TODO

## Preparando

[1]:https://www.djangoproject.com/
[2]:https://cx-oracle.readthedocs.io/en/latest/user_guide/installation.html
