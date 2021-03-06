# api-demo
Music App API contains songs by default in which user can register an account, search songs, create playlist and add songs to the playlist.

## DB Schema

![image](https://user-images.githubusercontent.com/52450550/146683104-fff953b4-8199-45db-8913-a1a185dd2dc7.png)


## Api Table

### Notations

* ip = localhost (for testing local)
* port = 5000 (port no taken from config.json)
* token = JWT token
* song = song to be searched
* pname = playlist name
* pid = playlist id
* sid = song id


Purpose  |  url  | Parameters |  Json |  Headers | Method
--- | --- | --- | --- | --- | ---
Signup | http://ip:port/signup | - | {'email':email, 'password:password}  |  -  |  POST
Get Token |  http://ip:port/auth/login |  -  | {'email':email, 'password:password} | - |  POST
Get All songs | http://ip:port/get/all/songs   | - | -| {'token':token} |  GET
Search   | http://ip:port/search/songs  | {'song_search':song} |  -  | {'token':token} |  GET
Create Playlist | http://ip:port/create/playlist | -  | {'playlist_name':pname}  | {'token':token} |  POST
Add Song | http://ip:port/add/playlist/songs  |  -| {'playlist_id':pid, 'song_id':sid}   | {'token':token} |  POST
Get Song | http://ip:port/get/playlist/songs   | {'playlist_id':pid}|  - | {'token':token} |  GET
Shuffle Playlist | http://ip:port/shuffle/playlist |  - | {'playlist_id':pid}   | {'token':token} |  POST



## How to run the program
* Install requirements.txt
* py app.py or flask run


## Note
* SongsList table will be loaded with default songs
* Token can be generated by /auth/login api which was mentioned in the table

## How to proceed
* Signup the user
* Generate token
* Enjoy the API! Cheers!
