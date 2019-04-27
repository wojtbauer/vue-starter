<template>

  <div >
  <h1>Witaj w systemie do zapisów na zajęcia!</h1>
  <div v-if="isAuthenticated">
    <p>Zalogowany jako {{ email }} </p>
    <button @click="LogOut()">Wyloguj</button>
  </div>
  <div v-else>
  	<input type="text" v-model="email">
 	<button @click="LogIn()">Zaloguj</button>

  </div>

  </div>
</template>

<script>
import "milligram";
export default {
	data() {
		  return {
		    email: '',
		    isAuthenticated: false
		  };
		},
		methods: {
				  LogIn() {
				    this.isAuthenticated = true;
				  },
				  LogOut() {
				  this.isAuthenticated = false;
				  this.email = '';
				}}
			
}
</script>

<style>

</style>
