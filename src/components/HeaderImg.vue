<template>
	<div class="headerImg">
	  <img :src="pictureUrl" alt="点击选择头像" />
	  <input type="file" class="file-button" @change="onFileChange" />
	</div>
</template>
<style></style>
<script>
	export default{
		data(){
	      return {
	        images:[],
	        pictureUrl:'../../static/img/headerImg.jpg'
	      }
	 	},
		methods:{
		    test () {
		    console.log(this.message)
		},
	    onFileChange (e) {
	      var files = e.target.files || e.dataTransfer.files
	      if (!files.length) return
	      this.createImage(files)
	    },
	    createImage (file) {
	      var vm = this
	      var reader = null
	      reader = new window.FileReader()
	      reader.readAsDataURL(file[0])
	      reader.onload = function (e) {
	        vm.pictureUrl = e.target.result
	      }
	    },
	  },
	}
</script>