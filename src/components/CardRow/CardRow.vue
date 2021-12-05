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
  <link
    href="https://fonts.googleapis.com/icon?family=Material+Icons"
    rel="stylesheet"
  />

  <a class="list-item" v-bind:href="this.href">
    <span id="list-item-icon" class="material-icons">{{ icon_name }}</span>
    <a id="list-item-link">{{ list_item_text }}</a>
  </a>
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
export default {
  props: {
    href: String,
    list_item_text: {
      type: String,
      default: "I am the default text",
    },
    icon_name: String,
  }
};
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
<style scoped>

.list-item {
  margin-top: 1.25rem;
  width: 30rem;
  text-decoration: none;
  display: flex;
  align-items: center;

  padding: 1rem;
  border-radius: 5px;

  background-color: var(--list-item-background-color);
  transition: var(--list-item-transition);
}

#list-item-link {
  font-size: 1.5rem;
  color: var(--list-item-color);
  text-decoration: none;

  transition: var(--list-item-transition);
}

#list-item-icon {
  color: var(--list-item-color);
  font-size: 2rem;
  padding-right: 1rem;

  transition: var(--list-item-transition);
}

.list-item:hover {
  background-color: rgb(160, 160, 160);
}

.list-item:hover #list-item-link,
.list-item:hover #list-item-icon {
  color: var(--list-item-color-on-hover);
}


/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .list-item{
    margin-top: 1.5rem;
    width: 20rem;
  }
  #list-item-link{
    font-size: 1.1rem;
  }

  #list-item-icon{
    font-size: 1.5rem;
  }

}
</style>

/* DEVELOPER NOTES: # I have used asci art as the comments # Learned v-bind, how
to use props to change href ( any attribute of an HTML ) element # Scoped to
make style spesific per component # Use '*{}' to be able to use CSS variables
while using scope in vuejs */
