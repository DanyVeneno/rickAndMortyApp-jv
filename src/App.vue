<template>
  <div>
    <h1>Rick & Morty</h1>

    <FilterByStatus />
    <FilterByName />
    <ListCharacters />

  </div>
</template>

<script>
import ListCharacters from '@/components/ListCharacters'
import FilterByStatus from '@/components/FilterByStatus'
import FilterByName from '@/components/FilterByName'

export default {
  name: 'App',
  components: {
   ListCharacters,
   FilterByStatus,
   FilterByName
    
  }
}
</script>

<style lang="scss">


:root{
  --background-body:#24282f;
  --background-card:#3c3e44
  --text-white:#efefef;
  --text-gray:#969696;
  --text-orange:rgb(160, 247, 78);
}
*{
box-sizing:border-box;
margin:0;
padding:0;

}
body{
  background-color: var(--background-body);
  color:var(--text-white);
  font-family:'Segoe UI','Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

}
h1{
  color:whitesmoke;
  margin-bottom: 3rem;
  text-align: center;
  margin-top:5rem;

}
.container{
  width:70%;
  max-width: 80%;
  margin:5rem;
}
img{
  width:100%;

}





</style>
