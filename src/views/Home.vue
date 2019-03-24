<template>
	<div class="home">
		<h1>HomePage</h1>
		<p class="red white--text">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
			tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
			quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
			consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
			cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
		proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
		<p class="pink lighten-4 red--text text--darken-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
		tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
		quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
		consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
		cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
		proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
		<h1 class="display-4">Massive Display</h1>
		<h4 class="display-1">Smaller Display</h4>
		<p class="headline">This is a headline</p>
		<p class="subeheading">This is a subheading</p>
		<p class="caption">This is caption</p>

		<v-btn class="pink white--text">Click me</v-btn>
		<v-btn depressed class="pink white--text">Click me</v-btn> <!-- removes the shadow -->
		<v-btn flat color="pink">Click me</v-btn> <!-- Makes the background transparent and color makes the text color pink -->
		<v-btn depressed round class="pink white--text">
			<v-icon left>email</v-icon>
			<span>Email me</span>
		</v-btn>

		<v-btn depressed round class="purple white--text">
			<span>Email me</span>
			<v-icon right>email</v-icon>
		</v-btn>

		<v-btn fab depressed round class="purple white--text hidden-md-and-down">
			<v-icon >email</v-icon>
		</v-btn>




		<v-speed-dial
      v-model="fab"
      :top="top"
      :bottom="bottom"
      :right="right"
      :left="left"
      :open-on-hover="hover"
      :transition="scale-transition"
    >
      <v-btn
        slot="activator"
        v-model="fab"
        color="blue darken-2"
        dark
        fab
      >
        <v-icon>account_circle</v-icon>
        <v-icon>close</v-icon>
      </v-btn>
      <v-btn
        fab
        dark
        small
        color="green"
      >
        <v-icon>edit</v-icon>
      </v-btn>
      <v-btn
        fab
        dark
        small
        color="indigo"
      >
        <v-icon>add</v-icon>
      </v-btn>
      <v-btn
        fab
        dark
        small
        color="red"
      >
        <v-icon>delete</v-icon>
      </v-btn>
    </v-speed-dial>






	</div>
</template>

<script>

export default {
    data: () => ({
      direction: 'top',
      fab: false,
      fling: false,
      hover: true,
      tabs: null,
      top: false,
      right: true,
      bottom: true,
      left: false,
      transition: 'slide-y-reverse-transition'
    }),

    computed: {
      activeFab () {
        switch (this.tabs) {
          case 'one': return { 'class': 'purple', icon: 'account_circle' }
          case 'two': return { 'class': 'red', icon: 'edit' }
          case 'three': return { 'class': 'green', icon: 'keyboard_arrow_up' }
          default: return {}
        }
      }
    },

    watch: {
      top (val) {
        this.bottom = !val
      },
      right (val) {
        this.left = !val
      },
      bottom (val) {
        this.top = !val
      },
      left (val) {
        this.right = !val
      }
    }
  }

</script>
<style>
.v-speed-dial {
    position: absolute;
  }

 #create .v-btn--floating {
    position: relative;
  }
</style>
