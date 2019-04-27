<template>
   <div>
       <p>Zalogowany jako {{ username }}</p>
       <button @click="$emit('logout')">Wyloguj</button>
       <h2>Spotkania</h2>
       <ol>
        <li v-for="meeting in meetings">
          {{meeting}}
       </li>
       </ol>
   </div>
</template>

<script>
export default {
 props: ['username'],
 data() {
	 return {
		 meetings: [
			 'MWO',
			 'TO'
		 ]
	 };
 }

}
</script>