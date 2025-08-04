For your code to run in a remote cloud server, the server must have all languages, modules etc. installed to run
To run your code perfectly we need to convert it to executable format (Called __*Building*__) Ex : [[Maven]]
So these are the steps :
#### Development --> pushing to github --> Extracting from github --> Building --> Testing the new Build --> Deploy the Build
for Building process its usually converting the .js --> executable for better performance and shipping it

some examples for building :
- mvn install (java) 
- npm run (NodeJS)
- webpack
etc... 

![[maven1.png]]
After building it is testing if executable is working fine or not and then it is deployed

