"# university" 

https://www.youtube.com/playlist?list=PLlKID9PnOE5jiWTTsshCXdz5qvg8JWezX

docker compose -f .\docker-compose-local.yaml up -d

image: mirror.gcr.io/postgres:14.1-alpine

===================
alembic init migrations
alembic.ini
sqlalchemy.url = postgresql://postgres:postgres@localhost:5432/postgres
env.py
from main import Base
target_metadata = Base.metadata

alembic revision --autogenerate -m "comment" - делается при любых изменениях моделей
alembic upgrade heads - применение
======================