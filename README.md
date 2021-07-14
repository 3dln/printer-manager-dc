# Orchestration for restaurant printer management

## Steps to run this project

### dev
- database
  - docker run -itd -p 5432:5432 -e POSTGRES_PASSWORD=root -e POSTGRES_USER=postgres -e POSTGRES_DB=cafe_db postgres
- app
  - npm run dev

### production
- Install docker for windows
- clone this repo
- cd into cloned directory
- git submodule update --init --recursive
- docker-compose up -d


