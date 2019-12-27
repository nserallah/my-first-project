<template>
    <div>
        <button class="modal-btn" @click="activeModal = '1'">
            <slot name="slot-button"></slot>
        </button>
        <transition name="bounce">
            <div class="overlay" v-if="activeModal === '1'">
                <div class="modal-box">
                    <div class="modal-header">
                        <button class="close-btn" @click="activeModal = '0'">close</button>
                        <h2>modal title</h2> 
                    </div>
                    <div class="modal-body">
                        <slot name="slot-body"></slot>  
                    </div>
                    <div class="modal-footer">
                        <button @click="activeModal = '0'">Cancel</button>
                        <input type="submit" value="save">
                    </div>
                </div>
            </div>
        </transition>
    </div>
</template>

<script>
export default {
    name:'popUp',
    data: function () {
        return {
           activeModal: '0' 
            
        }
    }   
}
</script>

<style scoped>

.modal-btn {
    float: left;
    padding: 10px 30px;
    margin: 10px
}

.close-btn {
    padding: 5px 10px;
}

.overlay{
    position:absolute;
    top:0;
    left:0;
    right:0;
    bottom:0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, .6);
}

.modal-box {
    position: relative;
    top:50%;
    left:50%;
    transform: translate(-50%, -50%);
    background-color: #fff;
    color: #000;
    height: 400px;
    width: 300px;
    border-radius: 20px 
}
.modal-box .modal-header{
    padding: 20px;
    height: 20%;
    border-bottom: 1px solid #000;
}
.modal-box .modal-header button {
    float: left;
}

.modal-box .modal-body {
    height: 60%;
    border-bottom: 1px solid #000;
    padding: 20px;
}
 
.modal-box .modal-footer {
    height: 20%;
    padding: 20px;
}

.modal-box .modal-footer button,
.modal-box .modal-footer input{
    padding: 5px 10px;
    margin: 0 5px;
}
/* this for fade transition tag to fade */
.bounce-enter-active {
  animation: bounce-in .5s;
}
.bounce-leave-active {
  animation: bounce-in .5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
  }
}

</style>