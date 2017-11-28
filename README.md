# GoGamers
We plan to make an online game based on the board game, “telestrations”. A group of people start with a prompt and a small drawing canvas. After drawing their prompt in a short amount of time, they pass their drawings in a circle. With the new drawing in hand, they write a description of what they think their drawing is. This repeats over and over until everyone gets a list back of all the drawings/descriptions that were formed from their starting drawing.

The project will be split into two main parts: client-side and server-side. The client-side will be responsible for providing an interface for the user to sign in or create an account, establishing a websocket connection with the server, displaying relevant messages from the server (like game state, other users moves, the drawings from other users, the game timer) as well as allowing the user to draw/write in their responses and push that data to the server. The client-side will also be responsible for allowing the user to edit their profile and view their favorite and/or winning drawings. There will be another feature during games where the users can communicate in a chatroom to leave kind words of encouragement.

The server-side will be responsible for handling authentication requests from the client, as well as storing user and session data in a mongo and redis database. The server-side will allow clients to upgrade their requests to websockets and then use those connections to arbitrate gamestate information (round timer, drawings/descriptions to and from users, game beginning and ending) between users and the server, and between users. Once a round has ended, the server will present each “stack” of drawings/descriptions to all users so that they can favorite the best drawings and pick the winning stack. The server will also use the same websocket connection to handle the chatroom where users are communicating during a game. Other functionality the server may have is to be able to change your user profile information, delete your account, and allow users who have joined the server to spectate while they wait for the current game to end. 

**Kyle:** Server Focused 

**Alex:** Server Focused 

**Jordan:** Client Focused 

**Calvin:** Client Focused 
