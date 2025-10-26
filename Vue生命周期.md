**Vue生命周期：一个Vue实例从创建到销毁的整个过程**

**生命周期的四个阶段：1.创建2.挂载3.更新4.销毁**

**1.创建阶段，响应式数据，*发送初始化渲染请求*2.挂载阶段，渲染模板，*操作dom*3.更新阶段数据修改，更新视图4.销毁阶段，销毁实例**

**Vue生命周期过程中，会自动运行一些函数，被称为生命周期钩子，让开发者可以在待定阶段运行自己的代码。**

**1.create、mounted、updated、destoryed**

**create和mounted**

**create:响应式数据准备好了，可以开始发送初始化渲染请求**

**通过V-for动态渲染页面中的数据。**

**V-bind动态绑定图片路径**

**四个阶段，八个钩子—>三个常用created,mounted,beforeDestory**

<script>
        const app=new Vue({
            el:'#app',
            data:{
                count:100,
                title:'计数器'
            },
            //1.创建阶段（准备数据）
            beforeCreate(){
               console.log('beforeCreate响应式数据准备好之前',this.count);

            },
            created(){
                console.log('create响应式数据准备好之后',this.count);
                //this.数据名=请求回来的数据
                //可以开始去发送初始化渲染的请求
            },
             //2.挂载阶段（渲染模板）
             beforeMounted(){
                console.log('beforeMounted模板渲染之前',document.querySelector('h3').innerHTML);
                
             },
             mounted(){
                console.log('mounted模板渲染之后',document.querySelector('h3').innerHTML);
                //可以开始渲染dom
                
             },
             //3.更新阶段（数据变化）
             beforUpdate(){
                console.log('beforUpdate数据变化之前',documengt.querySelector('span').innerHTML);
             },
             update(){
                console.log('update数据变化之后',document.querySelector('span').innerHTML);
             },
             //卸载阶段
             beforeDestroy(){
                 console.log('beforeDestroy实例销毁之前',);
                 console.log('清除一些Vue以外的东西，比如定时器，事件监听器等');
             },
             destory(){
                console.log('destory实例销毁之后',this.count);
             }
        })
    </script>
