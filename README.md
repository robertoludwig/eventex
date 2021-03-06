# Eventex

Sistema de Eventos encomendado pela Morena.

[![Build Status](https://travis-ci.org/robertoludwig/eventex.svg?branch=master)](https://travis-ci.org/robertoludwig/eventex)
[![Code Climate](https://codeclimate.com/github/robertoludwig/eventex/badges/gpa.svg)](https://codeclimate.com/github/robertoludwig/eventex)

## Como desenvolver?

1. Clone o repositório.
2. Crie um virtualenv com Python 3.5
3. Ative o virtualenv.
4. Instale as dependências.
5. Configure a instância com o .env
6. Execute os testes

```console
git clone git@github.com:robertoludwig/eventex.git wttd
cd wttd
python -m venv .wtdd
source .wttd/bin/activate
pip install - r requeriments-dev.txt
cp contrib/env-sample .env
python manage.py test
```


## Como fazer o deploy?

1. Crie uma instância no heroku.
2. Envie as configurações para o heroku.
3. Defina uma SECRET_KEY segura para a instância.
4. Defina DEBUG=False
5. Configure o serviço de email.
6. Envie o código para o heroku.

```console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
# hbn.link/secret_gen
heroku config:set DEBUG=False
# configuro o email e depois...
git push heroku master --force
``` 
