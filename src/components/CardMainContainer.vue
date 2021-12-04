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
  <div class="main-container">
    <CardRowProfilePhoto />
    
    <CardRow 
      v-bind:href="'tel:+' + '19364009468'" 
      list_item_text="123 456 7899" 
      icon_name="phone"
    />
    
    
    <CardRow 
      v-bind:href="'https://www.github.com/FaikYY'" 
      list_item_text="Github/FaikYY" 
      icon_name="face"
    />


    <CardRow 
      v-bind:href="'https://www.instagram.com/bythewayimfaik/'" 
      list_item_text="Instagram/bythewayimfaik" 
      icon_name="tag"
    />
    
    
    <CardRow 
      v-bind:href="'mailto:' + 'faikyesilyaprak@outlook.com'" 
      list_item_text="faikyesilyaprak@outlook.com" 
      icon_name="email" 
    />
  
  </div>
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
<script>
import CardRow from './CardRow/CardRow.vue';
import CardRowProfilePhoto from './CardTop/CardTopProfile.vue';

export default {
  components: { 
    CardRow, 
    CardRowProfilePhoto 
    },
  name: 'CardMainContainer',
  props: {
    msg: String,
    initialCount: Number
  }
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
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main-container{
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
