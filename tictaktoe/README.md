Tic Tac Toe made in Rails 5 and Action Cable

Ruby Version : ruby 2.2.6p396 (2016-11-15 revision 56800) [i386-mingw32]
Rails Version : Rails 5.0.7
Database : Redis, mysql2
Bundler : Bundler version 1.16.6


To run it on Windows Machine :
1-Do the installations.
2-Run Redis server and set path for redis in advance settings.

Few points to consider :

1- To have the Action Cable part we need to do a bit of setting up in the following files
  - routes.rb
  - cable.js
2- We need a way to be able to keep track of the players and their moves, So we will uniquely identify a connection object, which gives us a way to determine the players in the channel. Later on, we can then access this identifier through the instance variable uuid.
  - Check the file application_cable/connection.rb

3- Subscribe and unsubscribe is done in game_channel.rb

4- Observe the coffeescripts and the models defined and the actions they are responsible for.

5- The UI design and Javascript has been copied from drifferent sources. You can check the sugar.js and animate.css in vendor directory.
