<template>
  <div class="modal-backdrop">
     <div class="modal">
        <div class="header">
          <h2>basic Modal</h2>
        </div>
        <div class="body">
            <img src="./success.png" style="display:flex;float:right;width:100px;">
            <div class="content">
                <h3>what a pity</h3>
            </div>
            
            <div class="input">
                <input type="date" name="">
                <input type="time" name="">
            </div>
            <div class="content"style="clear:both; ">
                <h3>funny</h3>
                <h3>happy</h3>
            </div>
        </div>
        <div class="editor_wrap">
            <vue-wangeditor id="editor"  v-model="content1" :init-content="initContent" :disabled="false"></vue-wangeditor>
        </div>
        <div class="footer">
            <button type="button" class="btn-close" @click="closeSelf">关闭</button>
            <button type="button" class="btn-confirm" @click="confirm">确认</button>
        </div>
    </div>
 
  </div>
</template>
<script type="text/javascript">
import VueWangeditor from 'vue-wangeditor-simple'
export default { 
        data(){
            return{
                initContent: 'somethinghere:',
                content1: '', // 包含html标签
            }
        },
        computed:{
        },
        methods:{
        },
    mounted() {
    },
    components: {
        VueWangeditor
    }
}
</script>
<style>
.modal-backdrop { 
    position: fixed; 
    top: 0; 
    right: 0; 
    bottom: 0; 
    left: 0; 
    background-color: rgba(0,0,0,.3); 
    display: flex; 
    justify-content: center; 
    align-items: center; 
}
.modal { 
    background-color: #fff; 
    box-shadow: 2px 2px 20px 1px; 
    overflow-x:auto; 
    display: flex; 
    flex-direction: column;
    border-radius: 16px;
    width: 700px;
} 
.header { 
    border-bottom: 1px solid #eee; 
    color: #313131; 
    justify-content: space-between;
    padding: 15px; 
    display: flex; 
} 
.footer { 
    border-top: 1px solid #eee; 
    justify-content: flex-end;
    padding: 15px; 
    display: flex; 
} 
.body { 
    position: relative; 
    padding: 20px 10px; 
    margin-left: 20px;
}
.input {
    float:left;
    padding: 5px;
    margin: 10px 0 0 5px;
    border: 1px solid #eee; 
}
.content{
    margin:5px;
}
.img {
    float:right;
}
.btn-close, .btn-confirm {    
    border-radius: 8px;
    margin-left:15px;
    width:50px;
    height: 30px;
}
.btn-close {
    color: #313131;
}
.btn-confirm {
    color: #fff; 
    background-color: #2d8cf0;
}
.editor_wrap {
    margin:5px;
}
 
 
</style>