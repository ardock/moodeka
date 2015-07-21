A little quizz app for Moodle developers who want to play with Polymer and Moodle. I connected Polymer Topeka (https://github.com/polymer/topeka / https://www.polymer-project.org/apps/topeka/) with Moodle.

Start hacking:
* clone the moodeka web service (https://github.com/mouneyrac/moodle-local_moodeka) in the local folder of your Moodle site.
* you likely want to test on localhost first, so get CORS chrome extension to bypass CORS errors: https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkiljbi?hl=en
* install moodeka on your web server and run it. It should work (don't use your admin user as by default you should not be able to get an admin token from login/token.php for a service different from the official app).
* hack moodeka
* build the app in two files only (they run faster) with: vulcanize -o build.html index.html --strip --inline --csp
* copy build.html (rename it in index.html) and build.js in your server, cordova webviewer...

TODO
----
obviously there are plenty of things to improve:
* fork the topeka element git rep and create a branch for it - instead to store the modified component folder. So we should be able to just call bower install to automatically download it.
* allow to go back from signout page
* implement the leaderboard from topeka
* some way to renew the quizzes once they are done
* * etc.
