# cs188-sustainable-fashion

## PosgresSQL Guide (macOS)
[installation link](https://www.postgresql.org/download/macosx/)

I utilized homebrew to install the latest version of PosgresSQL, but I also installed Postgress.app by following [this tutorial](https://www.youtube.com/watch?v=wTqosS71Dc4).
* Postgress.app is a "simple, native macOS app that runs in the menubar without the need of an installer. Open the app, and you have a PostgreSQL server ready and awaiting new connections. Close the app, and the server shuts down."

I initially tried to create a local database just to see if I could get it to work.
* After installing Posgress.app, to get the database setup, click on the `initialize` button to start the server (you will see some deafult databases). The tutorial has you connect to the user database under your name.
* Next "configure your $PATH to use the included command line tools (optional):"
    ```
    sudo mkdir -p /etc/paths.d &&
    echo /Applications/Postgres.app/Contents/Versions/latest/bin | sudo tee /etc/paths.d/postgresapp
    ```
* after this just reload the terminal so you can use this new command line tool
* type `"psql postgres://[enter your protocol here]/[enter database you want to connect to here]`
    * the protocol is the `[user you want to connect to]@localhost:5432` (this connects to localhost over port 5432, this is the default port for a Postgres database)
* now you should be inside of the database
* you can type `\conninfo` to make sure you are connected to the right database
* type `\q` to exit the database
* because we used the default configuration, we can just type `psql` and it will bring up this database again
* if you want to stop the server from running, go to the posgress app and press `stop`

## Supabase Guide

[supabase tutorial](https://www.youtube.com/watch?v=kyphLGnSz6Q)

[supabase website](https://supabase.com/)

Supabase Info
* Supabase is a BaaS (Backend as a Service)
    * You can abstract and fast track many of the tedious aspect of setting up the backend
    * Once you set up Supabase, you will already have a database 
    * Supabase is great since you do not have to build you own backend. Supabase will help develop everything for you, and introduce different menthods and functions that you can call in your front-end to execute functionality that you would normally have to serve to an endpoint in your backend 
    * It hosts the database completely for you 
    * to modify database, can use either the SQL editor or the Table editor
        * Table editor is more visual, SQL editor allows you to write some SQL commands 
    
* As of now I have setup the database on Supabase. Now the next step would be to connect the backend to the frontend extension. (go back to video tutorial at 20:43 to continue after frontend is done)
    * I would need to create a supabase client file inside of the project
        * Then import a file from the supabase package (need to install it)

* I have also looked into sharing the subabase backend with others though [this document](https://supabase.com/docs/guides/platform/access-control)
