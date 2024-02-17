# Sistema de autenticação utilizando o FastAPI, PostgreSQL e jwt.
Neste projeto de login são criados três endpoints, são eles: register, login e test auth. 
Endpoints: 
- `register`: são passados user e password possibilitando o cadastro de usuário no banco de dados.
- `login`: possibilita o usuário logar se user e password forem válidos, será retornado um jw token.
- `test auth`: utilizado para testar o token e se válido retorna o dado,  caso não retorna erro. 

Utilizei o poetry para gerenciamento de dependências no Python, uvicorn como servidor para rodar o FastAPI, sqlalchemy como orm, psycopg2-binary para conectar com o banco, alembic para criar migrations. As libs para autenticação utilizadas são passlib, python-jose, python-multipart.   

Alguns comandos de interesse para rodar neste projeto:
- `uvicorn app.main:app --reload`: rodar o projeto para realizar o cadastro, efetuar login e testar o token gerado.
- `alembic revision --autogenerate -m'comments about update'`: gerar uma migration atualizada.
- `alembic upgrade head`: rodar a migration para aplicar as alterações no banco de dados.
