<template>
    <div id="cont" class="container d-flex align-items-center justify-content-evenly justify-content-sm-around flex-sm-row flex-column-reverse">
        <div class="d-flex flex-column">
            <input @keyup.enter="gen()" v-model="text" type="text" class="mb-3" placeholder="e: https://youtube.com">
            <button @click="gen()" type="submit" class="mt-3">generate</button>
        </div>

        <div id="contqr d-flex align-items-center justify-content-center">
            <img :src="img" alt="qrcode">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Content',
    data(){
        return {
            text: null,
            img: 'http://api.qrserver.com/v1/create-qr-code/?data=youtube.com&size=200x200&bgcolor=72-99-230&color=255-255-255'
        }
    },
    methods: {
        async gen(){
            
            this.img = 'https://i.ibb.co/2FWgsQX/spinl.gif'

            if(!this.text){
                Swal.fire({
                    icon: 'error',
                    title: 'Oops...',
                    text: 'Something went wrong!'
                })
                return
            }

            this.img = await `http://api.qrserver.com/v1/create-qr-code/?data=${this.text}&size=200x200&bgcolor=72-99-230&color=255-255-255`
            
        }
    }
}
</script>

<style scoped>
    #cont {
        height: calc(100vh - 80px);
    }
    input {
        border-radius: 25px;
        border-color: #F72585;
        text-align: center;
        padding: 5px;
    }
    button {
        background: #F72585;
        color: #fff;
        font-weight: 600;
        padding: 5px;
        border-radius: 25px;
        border-color: #F72585;
    }
    #contqr {
        width: 250px;
        height: 250px;
    }
</style>