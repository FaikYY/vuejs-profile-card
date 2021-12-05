<!-- 
   /$$                                       /$$             /$$              
  | $$                                      | $$            | $$              
 /$$$$$$    /$$$$$$  /$$$$$$/$$$$   /$$$$$$ | $$  /$$$$$$  /$$$$$$    /$$$$$$ 
|_  $$_/   /$$__  $$| $$_  $$_  $$ /$$__  $$| $$ |____  $$|_  $$_/   /$$__  $$
  | $$    | $$$$$$$$| $$ \ $$ \ $$| $$  \ $$| $$  /$$$$$$$  | $$    | $$$$$$$$
  | $$ /$$| $$_____/| $$ | $$ | $$| $$  | $$| $$ /$$__  $$  | $$ /$$| $$_____/
  |  $$$$/|  $$$$$$$| $$ | $$ | $$| $$$$$$$/| $$|  $$$$$$$  |  $$$$/|  $$$$$$$
   \___/   \_______/|__/ |__/ |__/| $$____/ |__/ \_______/   \___/   \_______/
                                  | $$                                        
                                  | $$                                        
                                  |__/                                        
-->
<template>
  <img id="profile-photo" src="https://avatars.githubusercontent.com/u/63950761?v=4" alt="profile-photo">
  <br>
  <h1 id="title">Faik Yesilyaprak</h1>
  <h2 id="subtitle">Junior Front-End Developer</h2>
</template>

<!-- 
                               /$$             /$$    
                              |__/            | $$    
  /$$$$$$$  /$$$$$$$  /$$$$$$  /$$  /$$$$$$  /$$$$$$  
 /$$_____/ /$$_____/ /$$__  $$| $$ /$$__  $$|_  $$_/  
|  $$$$$$ | $$      | $$  \__/| $$| $$  \ $$  | $$    
 \____  $$| $$      | $$      | $$| $$  | $$  | $$ /$$
 /$$$$$$$/|  $$$$$$$| $$      | $$| $$$$$$$/  |  $$$$/
|_______/  \_______/|__/      |__/| $$____/    \___/  
                                  | $$                
                                  | $$                
                                  |__/                
-->
<script scoped>
export default {

}
</script>

<!-- 
             /$$               /$$          
            | $$              | $$          
  /$$$$$$$ /$$$$$$   /$$   /$$| $$  /$$$$$$ 
 /$$_____/|_  $$_/  | $$  | $$| $$ /$$__  $$
|  $$$$$$   | $$    | $$  | $$| $$| $$$$$$$$
 \____  $$  | $$ /$$| $$  | $$| $$| $$_____/
 /$$$$$$$/  |  $$$$/|  $$$$$$$| $$|  $$$$$$$
|_______/    \___/   \____  $$|__/ \_______/
                     /$$  | $$              
                    |  $$$$$$/              
                     \______/               
-->
<style>
    img{
      transition: var(--list-item-transition);
        width: 12rem;
        border-radius: 50%;

        border: 5px solid rgb(150, 150, 150);
    }

    h1{
      color: rgb(100, 100, 100);
      
      font-size: 3rem;
      font-family: monospace;

      margin-bottom: 0;
    }

    h2{
      color: rgb(130, 130, 130);

      font-size: 1.5rem;

      margin-top: .5rem;
    }

@media  only screen and (max-width: 600px) {
  img{
        width: 10rem;
        border-radius: 50%;
    }

    h1{
      color: rgb(100, 100, 100);
      
      font-size: 2rem;
      font-family: monospace;

      margin-bottom: 0;
    }

    h2{
      color: rgb(130, 130, 130);

      font-size: 1rem;

      margin-top: .5rem;
    }
}
</style>