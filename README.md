<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
  <title>Rooms Vue Page</title>
  <script>  




</script>
</head>
<body>

<!-- CDN installation of Vue.js -->
	<script src="https://cdn.jsdelivr.net/npm/vue@2.5.13/dist/vue.js"></script>
<!--The link to the CND can be found here: "https://v2.vuejs.org/v2/guide/installation.html#CDN" -->

  <header>
	   <div class="headerdiv">
			<img src="header Image.png" alt="Header Image">
		</div>
	</header>
  
<!-- NAVIGATION BAR -->
	<nav>
      <ul>
        <li><a href="Home.html">Home</a></li>
        <li><a href="Rooms.html">Rooms</a></li>
        <li><a href="Booking.html">Booking</a></li>
        <li><a href="About.html">About</a></li>
        <li><a href="Contact.html">Contact</a></li>
      </ul>
    </nav>
  


  
  <br>
  <br>
  <br>
  <br>
  <br>
  
  <!-- CONTAINER CONTAINING TEXT AND IMAGE ROOM 1 -->
  
<div class="Room-container">
  <img src="Room-Image.jpg" alt="Image">
<!-- VUE APP 1 -->
	 <div id="app1">
		<div class="R-info">
			<h1>{{product}}</h1>
		  
		  
			<p v-if="inStock">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
			
			<p v-else>This room is not currently available</p>
			
			<p v-if="onSale"> SALE!!!</p>

			

		</div>
	</div>
</div>

  <!-- CONTAINER CONTAINING TEXT AND IMAGE ROOM 2 -->

<div class="Room-container">
  <img src="Room-Image.jpg" alt="Image">
<!-- VUE APP 2 -->
	 <div id="app2">
		<div class="R-info">
			<h1>{{product}}</h1>
		  
		  
			<p v-if="inStock">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
			
			<p v-else>This room is not currently available</p>
			
			<p v-if="onSale"> SALE!!!</p>

			

		</div>
	</div>
</div>

  <!-- CONTAINER CONTAINING TEXT AND IMAGE ROOM 3 -->

<div class="Room-container">
  <img src="Room-Image.jpg" alt="Image">

<!-- VUE APP 3 -->
	 <div id="app3">
		<div class="R-info">
			<h1>{{product}}</h1>
		  
		  
			<p v-if="inStock">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
			
			<p v-else>This room is not currently available</p>
			
			<p v-if="onSale"> SALE!!!</p>

			

		</div>
	</div>
</div>
	
	
<!-- VUE APP 4 FEEDBACK -->	
<div id="app-4">
  <form @submit.prevent="submitFeedback">
    <input v-model="message" placeholder="Enter a question and we will get back to you" class="feedback-input" />
    <button type="submit">Submit</button>
  </form>

  <b-alert v-if="showConfirmation" variant="success" dismissible @dismissed="dismissConfirmation">
    Thank you for your question!
  </b-alert>
</div>


<script>
<!-- VUE APP 1 -->
var app1 = new Vue({
  el: '#app1',
  data: {
    product: 'Room Option 1', //Room Heading
    inStock: true, //Availability
    onSale: true, //Sale
    
  }
})


<!-- VUE APP 2 -->
var app2 = new Vue({
  el: '#app2',
  data: {
    product: 'Room Option 2',
    inStock: true,
    onSale: false,
    
  }
})

<!-- VUE APP 3 -->
var app3 = new Vue({
  el: '#app3',
  data: {
    product: 'Room Option 3',
    inStock: false,
    onSale: true,
    
  }
})

<!-- VUE APP 4 -->
var app4 = new Vue({
  el: '#app-4',
  data: {
    message: '',
    showConfirmation: false
  },
  methods: {
    submitFeedback: function () {
      // Perform actions with the submitted feedback here
      console.log('Feedback submitted:', this.message);
      
      // Show the confirmation message
      this.showConfirmation = true;
      
      // Clear the input field
      this.message = '';
    },
    dismissConfirmation: function () {
      // Dismiss the confirmation message
      this.showConfirmation = false;
    }
  }
});


 </script>	
	
 
<footer>
  <img src="Footer Image.png" alt="Footer Image">
  </footer>
</body>
</html>
