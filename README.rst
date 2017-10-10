.. image:: https://travis-ci.org/shuup/shuup.svg?branch=master
    :target: https://travis-ci.org/shuup/shuup
.. image:: https://coveralls.io/repos/github/shuup/shuup/badge.svg?branch=master
   :target: https://coveralls.io/github/shuup/shuup?branch=master

Loja PyLadies Brasil
====================

Instalando e Rodando
--------------------

- Assumindo que seu git já está configurado, faça o clone do repositório
    $ git clone git@github.com:pyladies-brazil/lojinha.git

- Dentro da pasta lojinha, crie uma nova virtualenv e ative-a
    $ python -m venv .venv
    $ source .venv/bin/activate

- Instale as dependências com pip
    $ pip install -r requirements-doc.txt

- Rode as migrações para criar o banco de dados e execute o projeto
    $ python manage.py migrate
    $ python manage.py shuup_init

Abra o browser em [localhost:8000](http://localhost:8000) para ver o conteúdo gerado.

Contribuindo
--------------------------------------

Para contribuir com o projeto veja o guia de [Contribuição](http://shuup.readthedocs.io/en/latest/howto/getting_started_dev.html).


Links Úteis
-----------

* Virtualenv - http://docs.python-guide.org/en/latest/dev/virtualenvs/
* Pyenv - https://github.com/yyuu/pyenv