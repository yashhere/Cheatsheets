What causes IRC to throw "nickname is already in use":
1.  You are not closed your previous session of IRC chat
     a) Trying to login with same nickname in another place/application with
          existing active connection.
2.  You are internet connectivity disconnected & IRC server not released
      your session.

How to fix:
a) /msg nickserv ghost <your_nickname> <password>
b) /msg nickserv <your_nickname>
b) /msg NickServ identify <password>
