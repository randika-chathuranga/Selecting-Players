<template>
<AppHeader/>
<div class="w-full flex">
<srilankan />
</div>
</template>
 

<script>

import AppHeader from './components/AppHeader';
import Srilankan from './components/Srilankan';


export default {
  components:{ AppHeader , Srilankan},  
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
   color: #2c3e50;

}
</style>
