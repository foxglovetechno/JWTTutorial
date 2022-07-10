# JWTTutorial

Secure Authentication in Node JS:-

1. Session Cookie :- In this case if you login using your credentials it’s gonna to the api and if the credentials are valid it’s gonna create a session and store it inside your server and give you a cookie that includes your session id. So whenever you attempt private end point for example update the user or delete the post or whatever. You’re gonna send this cookies to server and it’s gonna check whether the information matches with this session in the memory or not. If everything is ok you will be able to reach to the api
2. .JWT(JSON Web Token):- When you login with your credentials it’s gonna create a secret token that nobody can create and send you without storing it anywhere. When you try to delete your account you should provide this token in the header of your request and the server decodes and checks this token and decides whether this token is valid or not. It’s consists of three parts. First one is header part it’s includes our hashing algorithm.Second part is payload part it includes our id and any given payload here ex. You can provide your user id, username ,email whatever you want and this is issued at date. It shows when this token has been created also you can add an expiration date let’s say one day and after one day this token will be invalid and Finally third one is signature that includes our encoded script key. You can write any script key you want. 
3. Compare b/w:-We store the session on the server and each time a user login we should store a new one but the major problem is this session belongs that server. Now a days every applications  includes at least couple of micro services remember our social media application  we have an api server and chat server.so imagine you have an e-commerce web application you want to separate servers maybe you have normal shopping application and help desk application and maybe users can communicate with each other inside a forum application so all of these servers are independent so thanks to JWT it’s really easy to share token between different apps. In this case they all can use just one token and authorise your actions. So in a nutshell JWT is awesome and highly recommend to use it.