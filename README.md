# groupProject

Using Github so that we can all run and edit the same system. At the moment it's a simple database example from the docs.

kurtosis run github.com/coleraffell/groupProject/kurtosis-postgres '{"actors": [{"first_name":"Cole", "last_name": "Raffell"}]}'

will run the Kurtosis package on your own machine. This instance uses a database in which the first and last name will be added to. 

When this is run, you'll have your own enclave running on your network. Take a look at the port number it's running on:

98d9ef69569b   api        http: 3000/tcp -> http://127.0.0.1:54283             RUNNING

To query the database back:

curl -XGET "http://127.0.0.1:$PORT/actor?or=(last_name.eq.Raffell)"