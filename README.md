# A Node.js project which handles orders of a restaurant and sends bills to different printers

## Steps to run this project

### dev

- database
  - docker run -itd -p 5432:5432 -e POSTGRES_PASSWORD=root -e POSTGRES_USER=postgres -e POSTGRES_DB=cafe_db postgres
- app
  - npm run dev

### production

- Install docker for windows
- clone the main repo (not any submodules)
- cd into cloned directory
- git submodule update --init --recursive (this will add all submodules)
- docker-compose up -d (where docker-compose.yml file exists)

## TODO

- [x] Setup server with typescript and typeorm
- [x] Setup postgres
- [x] Setup docker and compose for orchestration
- [x] All interfaces
- [x] User model
- [x] Interactive header based on received data
- [ ] All routes
  - [x] Login
  - [x] get data
  - [ ] Add to basket
  - [ ] submit
  - [ ] autocomplete
- [x] Error management
- [ ] Logger
  - [x] api logger (morgan)
  - [ ] main logger (winston)
- [x] middlewares
- [x] validation
- [x] Category model
- [x] product model
- [x] Cart model
- [x] Order model
- [ ] cart page
  - [ ] cart functionalities
    - [ ] remove item
    - [ ] total price
    - [ ] delete cart
    - [ ] send cart
  - [ ] autocomplete box
    - [ ] prevent entering farsi chars
- [x] Login
- [x] User signout
- [x] Get Printers
- [x] Define Printers
- [ ] Next.js
  - [ ] Custom server
  - [ ] pkg
  - [ ] env
- [ ] Fonts
  - [x] farsi fonts
  - [ ] farsi digits
- [x] RTL
- [ ] Show parent title in product pages
- [ ] optimize and cache product images after first load to speed up
- [ ] Single source of truth architecture for offline mode
  - [ ] Save received info from server into client db
  - [ ] Client db is our single source of truth
  - [ ] Client db needs to get synced with server's db periodically
  - [ ] Check for internet connection availability
  - [ ] Sync menu items and customer data
    - [ ] When internet becomes available
    - [ ] On a regular basis (like every hour)
  - [ ] Error Handling
    - [ ] Server access is not available
    - [ ] Client db is not accessible
    - [ ] Syncing errors
