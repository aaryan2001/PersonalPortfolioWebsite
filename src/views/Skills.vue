<template>
    <div>
        <h1> Skills </h1>
        <input type="text" class="filter" v-model="desc" placeholder="Filter By Description"/>
        <br><br>
        <v-simple-table class="table table-hover">
			<thead>
				<tr>
					<th scope="col">Skillset</th>
					<th scope="col">Description</th>
                    <th scope="col">Rating</th>
				</tr>
			</thead>

			<tbody>
				<tr v-for="skill in getItems" :key="skill.set" >
					<td>{{skill.set}}</td>
					<td>{{skill.desc}}</td>
                    <td>{{skill.rate}}</td>
				</tr>
			</tbody>
		</v-simple-table>
        <br><br><br>
    <div>
	<paginate 
		:page-count="4"    
		:page-range="3" 
		:margin-pages="1"
		:click-handler="clickCallback" 
		:prev-text=" 'Prev' " 		
		:next-text="'Next'" 
		:container-class="'pagination'" 
		:active-class="'currentPage'"
	>
	</paginate>
	</div>
	
    </div>  
</template>

<script>
	import Vue from 'vue'
	import Skills from "../assets/skills.json";
	import Paginate from 'vuejs-paginate';
	Vue.component('paginate', Paginate);

	export default {
	name: 'Skills',
	data: function(){
		return {
            desc:'',
			currentPage: 1,
			skills:Skills,
            kills: []
		}
		},
	computed: {
    filterDesc: function() {
                return this.skills.filter(skill => !skill.desc.toLowerCase().indexOf(this.desc.toLowerCase()))
            },
     getItems: function() {
        let current = this.currentPage * 4;  // total 16 skills, suppose 4 per page, 4 pages
        let start = current - 4;
        return this.filterDesc.slice(start, current);
      }
	},
    methods: {
      //sets the clicked page
      clickCallback: function(pageNum) {
        this.currentPage = Number(pageNum);
      }
    }

}
</script>

<style>

.pagination{
    float:center;
    margin: 5% 40%;
}
.pagination a {
  color: black;
  border: 1px solid #ddd;
  padding: 8px 16px;
  text-decoration: none;
}
.currentPage a {
  background-color:lightblue ;
}
.filter{
	border-style: solid;
	text-align: center;
}
@media screen and (max-width: 800px) {
.pagination {margin:0 0;}
}
</style>