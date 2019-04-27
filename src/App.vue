<template>

  <div >
  <h1>Witaj w systemie do zapisów na zajęcia!</h1>
  <div v-if="email.length > 0">
 	<LogoutForm :username="email"
 			@logout="LogOut()"></LogoutForm>
  </div>
  <div v-else>
   <login-form @login="LogIn($event)"
   				header="Zaloguj sie"
   				button-label="Log in"></login-form>
   <login-form @login="LogIn($event)"
   	  			header="Zarejestruj sie"
   				button-label="Log up"></login-form>
   
  </div>

  </div>
</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";
import LogoutForm from "./LogoutForm";

export default {
	components: {LoginForm, LogoutForm},
	data() {
		  return {
		    email: '',
		  };
		},
		methods: {
				  LogIn(username) {
					this.email = username;
				  },
				  LogOut() {
				  this.email = '';
				}}
			
}
</script>

<style>

</style>
