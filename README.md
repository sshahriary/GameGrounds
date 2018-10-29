# GameGrounds
proof of concept for a platform to search, challenge, and rate peers
## System needs
  * Data store
  * Middle tier: Access Data/Api's
  * UI: presentation
  * Security
  
### Data store needs
  * Free
  * text based searches
  * Scalability(grow as needed, add machines if neccessary)
#### Info to store
  * **MySQL**
    + email!
    + password!(encrypted)
    + User Picture
    + Name
    + Verified players (chosen by Admin)
    + Unique MySQL ID to tie data to User for Elastic Search
    + for future: phone #, credit card #, paypal... etc.
    + gaming categories (provided to user): Sports, Action, Strategy, Adventure
    + games (Including different versions up to 3 years, provided to user): FIFA, NBA, Madden, World of Warcraft, League of Legends, Call of Duty
    + Platform (Provided to user): Xbox, PS4, PC **Note:** User provides GamerTag for each platform but preffered Platform Gamertag is visible for search.
    + Rating: 1 - Novice, 2 - Intermediate, 3 - Expert. Able to add more in future: professional(Verified)
  * **Elastic Search**
    + User attributes: Name, Unique ID, Games played and their Categories, own Rating, peer Rating(Keep count next to ratings), flag for verified.
    
#### Features
  * **search**
    + __Platform__ | __Game Catgeories__ | __Player Tag__ | __Game__ | __Version__ | __Level__
    + When you find player on search, it displays their preffered platform gamerTag
  * **Public User Page** 
    + Page to display all user's info
  * **Message System**
    + To be able to contact and challenge players
  * **Rating Others**
    + Input which platform, Game, GamerTag, and rate on scale from Novice to Expert.
    + Success or failure depending on whether fields are correct
   
#### Requirements
  * Unregistered users can search users, look at rating, look at games played. Can NOT interact with players.
