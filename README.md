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
