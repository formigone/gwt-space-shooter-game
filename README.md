### Welcome to Space Shooter.

Space Shooter is arcade shooter game with pumping skills elements where player attempts to survive as long as possible 
and destroy maximum count of asteroids. Every time you kill an asteroids you gain experience. 
At the beginning player appear at the center of the game field with some count of health and without experience points.

### Here's a spaceship. There are the asteroids. Good luck, commander!

That's about your missions statement in Space Shooter. The game presents you a 2D world. 
You are the lonely commander of the spaceship in the middle of the universe, 
the asteroids and bonuses start pouring from top of the map. The count of this object is growing with new experience. 
Collision between asteroids and ship takes a player's health. 
Asteroids have a different walking speeds. The game ends when a player takes the last health, 
the best result will be added to the cookies and extract from here at the start of the game and displayed in a 
special info box.

### Controls:

 - Esc - pause
 - Shift key or left mouse button - fire
 - Ctrl - enable/disable the position information of elements
 - Mouse move or arrow keys (up, down, left, right) - spaceship movement

### Power-ups:

Powerups or bonuses allow to add extra abilities to the player for some time as a game mechanism.
 - medpacks - pick this up and you get one more health back instantly
 - freeze - the asteroids are frozen for some time
 - reflex boost -  the reflex boost slows asteroids in the game down except for your movement
 - shield - with the shield powerup you are invulnerable for a short period of time
 - double experience - when this powerup is active, you get double experience from destroyed asteroids

Bonuses are very important for game process, they are very helpful in difficult situations and add dynamic and interesting to the gameplay. 
Time bonus lasts for 5 seconds after contact with the ship. You can not take two of the same bonus, until the end time. 
But you can take all the bonuses at once, but only one type. End time of the bonuses will be displayed to the user on the game field. 

### Audio: 

The game has a background music and the sound of the collision. There are some really good old school 8-bit 
tracks that really gets you specific atmosphere. The magic of the sound was done using [`gwt-voices`](http://code.google.com/p/gwt-voices/) library.  

### GWT Linker
I'm a little bit experimented with HTML5 offline browsing support and as example upload this feature to the game.
Almost all code can be find in [linker](https://github.com/dmitrynikol/gwt-space-shooter-game/tree/master/src/com/dmitrynikol/spaceshooter/client/linker) package. 
Documentation for [offline web applications](http://www.w3.org/html/wg/drafts/html/master/browsers.html#offline).

To make GWT application runs offline need to write a custom linker.
On every compile, linker regenerate the spaceshootercache.manifest file with files from the public path of the module.

Main module SpaceShooter.gwt.xml contains properties with <extend-configuration-property /> tag.
[LinkerContext](http://google-web-toolkit.googlecode.com/svn/javadoc/2.5/com/google/gwt/core/ext/LinkerContext.html) used to get ConfigurationProperty, it contains all configuration property values in the 
module. It provides access to data about the linking process. 
And method PersonalLinker#getPropertiesExtraFiles() get array of configured external properties.


Feel free to use this code to get your GWT game up and running.