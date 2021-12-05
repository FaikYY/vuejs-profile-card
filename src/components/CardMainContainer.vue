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
  <div :class="{darkMode: is_darkMode_active}" class="main-container" >
   
    <button id="darkMode-toggle-on" v-if="is_darkMode_active" @click="toggle_darkMode">ON 🌙</button>
    <button id="darkMode-toggle-off" v-else @click="toggle_darkMode">OFF 🌙</button>
    <CardRowProfilePhoto />
    
    <CardRow 
      v-bind:href="'tel:+' + '11234567899'" 
      list_item_text="123 345 7899" 
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
    CardRowProfilePhoto,
    // DarkMode
    },
  name: 'CardMainContainer',
  props: {
    msg: String,
    initialCount: Number
  },
  data: function() {
    return{
      is_darkMode_active: false
    }
  },
  methods:{
    toggle_darkMode(){
      this.is_darkMode_active = !this.is_darkMode_active;
    }
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
<style>
* {
  --list-item-color: rgb(100, 100, 100);
  --list-item-background-color: rgb(220, 220, 220);
  --list-item-color-on-hover: rgb(235, 235, 235);
  --list-item-transition: 0.15s ease-in-out;

  --list-item-color-darkMode: rgb(150, 150, 150);
  --list-item-background-color-darkMode: rgb(30, 30, 30);
  --list-item-on-hover-darkMode:  rgb(15, 15, 15);
}

.main-container{
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  transition: .2s ease-in-out;
}

#darkMode-toggle-on{
  padding: 1rem;
  font-size: 1rem;

  background-color: rgb(60, 60, 60);
  color:  rgb(240, 240, 240);
  
  border: none;
  border-radius: 10px;
  
  position: absolute;
  top: 5rem;
  right: 5rem;
}

#darkMode-toggle-off{
  padding: 1rem;
  font-size: 1rem;

  background-color: var(--list-item-background-color);
  color: rgb(60, 60, 60);
  
  border: none;
  border-radius: 10px;
  
  position: absolute;
  top: 5rem;
  right: 5rem;
}
/* DARK MODE STYLES */
.darkMode{
  background-color: rgb(15, 15, 15);
}

.darkMode h1{
  color: white;
}

.darkMode .list-item{
    color: var(--list-item-color-darkMode);
    background-color: var(--list-item-background-color-darkMode);
}

.darkMode .list-item:hover{
    background-color: rgb(60, 60, 60);
}

.darkMode #list-item-link,
.darkMode #list-item-icon{
  color: var(--list-item-color-darkMode);
}

.darkMode #profile-photo{
  border: 5px solid rgb(100, 100, 100);
}

.darkMode #title{
  color: rgb(180, 180, 180);  
}

.darkMode #subtitle{
  color: rgb(160, 160, 160);
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  #darkMode-toggle-on{
  font-size: .8rem;
  padding: .8rem;

  background-color: rgb(60, 60, 60);
  color:  rgb(240, 240, 240);
  
  border: none;
  border-radius: 10px;
  
  position: absolute;
  top: 4rem;
  right: 3rem;
}

#darkMode-toggle-off{
  font-size: .8rem;
  padding: .8rem;

  background-color: var(--list-item-background-color);
  color: rgb(60, 60, 60);
  
  border: none;
  border-radius: 10px;
  
  position: absolute;
  top: 4rem;
  right: 3rem;
}
}
</style>
