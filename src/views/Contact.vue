<template>
<div>
    <div class="container">
    <br>
        <div class="row">
            <br>
            <br>
            <h2>Follow me on</h2>
            <p><a href="https://www.facebook.com/aaryanpujara.7/">Facebook</a></p>
            <p><a href="https://www.instagram.com/aaryan_pujara/">Instagram</a></p>
            <p><a href="https://www.linkedin.com/in/aaryan-pujara-5931bb192/">LinkedIn</a></p>
            <br>
        </div>
    </div>
    <br>
    <h1> Submit a query </h1>
    <br>
    <div class="container">
    <br>
        <div class="row">
            <br>
            <form method="post"
            action="https://mercury.swin.edu.au/it000000/formtest.php" novalidate >
            <label for="fname">  First name:  </label>
            <input type="text" id="fname" name="fname">
            <label for="lname">  Last name:  </label>
            <input type="text" id="lname" name="lname">
            <label for="email">  Email:  </label>
            <input type="text" id="email" name="email"><br><br>
            <p>Message:</p>
            <textarea name="message" rows="10" cols="30"></textarea><br><br>
            <input type="submit" value="submit">
            </form>
            <br>
        </div>
        <br>
    </div>

    <div><br>
    <h1>Leave a comment or feedback.</h1>
	<p>Comment: <input type="text" id="status" v-model="strStatus"/> 
	<button @click="add(strStatus)">Publish</button></p> 
	<div v-for = "(i,index) in statPosts" :key="i">
	<p>{{i}} <button @click="remove(index)">Delete</button></p>
	</div></div>
</div>
</template>

<script>
	export default {
		data:function(){
		return{
			statPosts:[],
			strStatus:''
		}
},
methods:{
		add:function(status){
			this.statPosts.push(status)
},
		remove:function(index){
		this.statPosts.splice(index,1)}
	}
}
</script>