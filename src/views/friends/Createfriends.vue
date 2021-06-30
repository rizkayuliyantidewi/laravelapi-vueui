<template>
<div class="card shadow mt-3">
  <div class="card-body">
<<<<<<< HEAD
    <h5 class="card-title">Add friends</h5>
=======
    <h5 class="card-title">Add friend</h5>
>>>>>>> decce96ef64dac53f79078783cfb4f2f7fc3f241
     <form class="row g-3"  @submit.prevent="store">
    <div class="col-md-6">
      <label for="inputEmail4" class="form-label">Nama</label>
      <input type="text" class="form-control" id="inputEmail4" />
      v-model="friend.nama"/>
      <div class="alert alert-danger" v-if="validation.nama">
        {{ validation.nama[0] }}
        </div>
    </div>
    <div class="col-md-6">
      <label for="inputPassword4" class="form-label">No Tlp</label>
      <input type="number" class="form-control" id="inputPassword4" />
<<<<<<< HEAD
        v-model="friend.no_tlp"/>
=======
        v-model="friend.nama"/>
>>>>>>> decce96ef64dac53f79078783cfb4f2f7fc3f241
      <div class="alert alert-danger" v-if="validation.no_tlp">
        {{ validation.no_tlp[0] }}
        </div>
    </div>
    <div class="col-12">
      <label for="inputAddress" class="form-label">Alamat</label>
      <input type="text" class="form-control" id="inputAddress" placeholder="Masukan alamat"
        v-model="friend.alamat"/>
      <div class="alert alert-danger" v-if="validation.alamat">
        {{ validation.alamat[0] }}
        </div>
    </div>
    
    <div class="col-12">
      <button type="submit" class="btn btn-primary">Add</button>
    </div>
  </form>
  </div>
</div>
 
</template>
<script>
import { reactive, ref } from 'vue';
import { useRouter } from 'vue-router'
import axios from 'axios'
export default {
   setup() {
     const friend = reactive({
       nama: '',
       no_tlp:'',
       alamat:''

     })
     const validation = ref([])
     const router = useRouter()
     function store (){
       let nama = friend.nama
       let no_tlp = friend.no_tlp
       let alamat = friend.alamat
<<<<<<< HEAD
       axios.post("http://pia.labirin.co.id/api/friends/", {
=======
       axios.post('http://127.0.0.1:8000/api/friends', {
>>>>>>> decce96ef64dac53f79078783cfb4f2f7fc3f241
         nama: nama,
         no_tlp: no_tlp,
         alamat: alamat
       }).then( () => {
         router.push({
<<<<<<< HEAD
           name:'Home',
=======
           name:'Home'
>>>>>>> decce96ef64dac53f79078783cfb4f2f7fc3f241
         })
       }).catch(error => {
          console.log(error)
       })
     }
     return {
       friend,
       validation,
       router,
       store
     }
   },
}
</script>

