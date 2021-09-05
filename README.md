# Oxytocin
Full-Stack Project for oxytocin

## The server is hosted at https://oxytocin-fullstack.herokuapp.com/

## to run the server locally
1. Clone the repository
```
git clone https://github.com/sourabh112/Oxytocin.git
cd Oxytocin
```
2. Install the required node modules and dependencies
```
npm install
```
3. Download the ngrock from https://ngrok.com/download
4. Run the ngrock server
```
ngrock.exe http 5000
```
5. Update the Twillio Whatsapp settings "WHEN A MESSAGE COMES IN" with the ngrock server url
6. Download PostgresSql from https://www.postgresql.org/download/
7. Create 2 tables using these commands in postgresql server or use GUI in shops_databse
```
CREATE TABLE IF NOT EXISTS public.cache_memory
(
    id text COLLATE pg_catalog."default" NOT NULL,
    name numeric NOT NULL,
    product numeric NOT NULL,
    inventory numeric NOT NULL,
    menu numeric NOT NULL,
    p_id text COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT cache_memory_pkey PRIMARY KEY (id)
);

CREATE TABLE IF NOT EXISTS public.shops
(
    id text COLLATE pg_catalog."default" NOT NULL,
    name text COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT shops_pkey PRIMARY KEY (id)
);
```
8. Update the code lines according to your database settings : https://github.com/sourabh112/Oxytocin/blob/97ddbb068a3c27f50e99d3e80523ccb36e6aab44/script.js#L9-L18
9. Finally run 
```
npm start
```
10. If something dosen't work you are welcomed to create a issue.


messenger.js only contains only dummy twillo Authentication and Account ID. Change them to your Authentication and Account ID in order to get your bot to work. And Start with activate your bot (In ngrock tutorial).
