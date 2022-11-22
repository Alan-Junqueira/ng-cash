# ng-cash

🛠️ Abrir e rodar o projeto

### Se for usar o Docker

git clone nesse repositório, para pegar a configuração do docker-compose.yml

Dentro da pasta que fizer o clone deste arquivo, clonar o frontend e o backend e renomear as pastas.
A pasta do projeto do frontend deve ser renomeada para frontend.
A pasta do projeto do backend deve ser renomeada para backend.

Clone do frontend:
git clone git@github.com:Alan-Junqueira/ng-cash-frontend.git

Clone do backend:
git clone git@github.com:Alan-Junqueira/ng-cash-backend.git

Com todos os projetos clonados e na sua máquina, é necessário fazer alguns pequenos ajustes.

No arquivo Dockerfile do projeto do frontend e do projeto do backend, o WORKDIR deve ser alterado de acordo com sua maquina.

No meu frontend por ex, está assim o Dockerfile: WORKDIR /home/alan/development/ng-cash/frontend

No seu caso, deve modificar para especificar o local que esta na sua maquina.

Verifique se a formulação das pastas está identica à formulação deste projeto.

-frontend
-backend
-.dockerignore
-docker-compose.yml

Caso esteja...

Na raiz, digite na pasta que esta o docker-compose.yml:

docker-compose build (aguarde a criação)
docker-compose up ou docker-compose up -d

Pronto, containers rodando, basta acessar a aplicação e ver funcionando.

### Se não for usar o Docker

Clone do frontend:
git clone git@github.com:Alan-Junqueira/ng-cash-frontend.git

Clone do backend:
git clone git@github.com:Alan-Junqueira/ng-cash-backend.git

npm run dev em ambos projetos.

O backend vai rodar na porta 3333.
O frontend vai rodar na porta que o vite estipular. (costuma ser a 3000)
