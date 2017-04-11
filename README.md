# pubg
 Playerunknown’s Battlegrounds Websocket API example


WARNING: READ GNU General Public License v3 (GPL-3)  



Deps: npm install ws underscore express body-parser



How to get ticket (aka access token aka password?):

1) Run wireshark, filter by: tcp.port == 81 && http

2) Run game and wait for loading menu (lobby)

3) Looking for something like "/userproxy?provider=steam&.." in wireshark and open it (by left click)

4) Copy Value from middle frame, it's must be more 450 symbols (468 for me)

You can found full lenght ticket in "Request URI Query Parameter",press right mouse -> copy -> value and remove "ticket="



Ticket will dead after few minutes in offline (sure, maybe ip change need to regenerate token). OR it maybe works while you in game.

You need start game again and get ticket again.

You can be connected with out any problems for few hours and do fast restarts if u need this. 

Not possible to play while connected from this script (not sure about real play, but you will be kicked from lobby by double connection)



More methods here: https://gist.github.com/Hormold/92fbb9733eb9c9f0fef9adf0e0750bc7

If you will found how to generate token from engine - it'll be cool!

Look at the menu(lobby) source code here: http://front.battlegroundsgame.com/app/2017.04.06-4/app.js

Get more info about game protocol using Wireshark and filter: (websocket)
