# appstore-ui-4553-patch

INTRODUCTION:-  This Patch is used for get appstore UI in released unravel versions - 4.5.5.3.
Base Branch for UI:  appstore/4.5.5.3 

Steps for Patching - 4553

 1.  Download all files 
www.zip
server.zip
node_modules.zip
appstore-patch-4533.sh
appstore-rollback-4553.sh (Optional)

 2. Run the Patch Script 
  Command :-  ./appstore-patch-4533.sh --user <username>
  Ex. ./appstore-patch-4533.sh --user hdfs

 3. Rollback the Patch (If required)
 Command :- ./appstore-rollback-4553.sh --user <username>
    Ex. ./appstore-rollback-4553.sh --user hdfs




======================================================

 Create steps of www.zip & server.zip :-

 Make an RPM from git branch appstore/4.5.5.3

 Deploy in any cluster
      
 Make a zip of /usr/local/unravel/ngui/www, /usr/local/unravel/ngui/server
  command :-  zip -r  www.zip /usr/local/unravel/ngui/www
                       zip -r  server.zip /usr/local/unravel/ngui/server



 Create steps of node_modules.zip :-

Install nodejs (version : v6.10.0)  in your system 

Run the command :npm install multer 

Make a zip node_modules
  Command: zip -r node_modules.zip node_modules
