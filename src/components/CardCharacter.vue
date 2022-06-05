<template>
  <div class="character">
      <img :src="character.image" :alt="character.name">

      <div class="character_info">
          <h4>{{ character.name }}</h4>
          <div class="status">
              <span
                  :class="
                    character.status == 'Alive' ? 'alive' :
                    character.status == 'Dead' ? 'dead' :
                    'default'
                  
                  "
                  >
              </span>
              <span>{{character.status}} - {{character.species}}</span>
          </div>
          <div class="origin">
              <span>
                  Origin:
                  {{character.origin.name}}
              </span>
          </div>



      </div>
  </div>
</template>

<script>
export default {
    props:['character']

}
</script>

<style>
.character{
  background-color: var(--background-card);
  border-radius: 20px;
  box-shadow: 0 0 10px 1px var(--background-body);
  overflow: hidden;
  cursor: pointer;
  transition:transform 200ms ease-in-out;
  height:100%;
}
  .character:hover {
    transform: scale(1.05);
  } 
  
  h4 {
      color: var(--text-orange);
    }
  span{
    color: var(--text-gray);
  }
  h4{
    margin-bottom: 0.5rem;
  }
  .character_info {
    padding:1.5rem;
  }
    .status {
      display: flex;
      align-items: center;
      margin-bottom: 0.5rem;
    }
  span {
      color: var(--text-gray);
      }
    span:first-child {
          width: 10px;
          height: 10px;
          border-radius: 50%;
          margin-left: 0.5rem;
        }

      
 .alive{
   background-color:greenyellow;
 }
 .dead{
   background-color: tomato;
 }
.default{
  background-color: whitesmoke;
 }


.origen {
  margin-bottom:0.5rem;
}
  



</style>