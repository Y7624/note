Geeter不应该爱有副作用

**不要改变其他状态，在getter中做异步或者更改dom**

getter的职责仅为计算和返回该值

<MyComponent v-for="item in items" :key="item.id" />

key绑定的值是一个基础类型的值，不要用对象作为v-for的key

key在这里是一个通过v-bind绑定的attribute，请不要和v-for使用对象里所提的属性名混淆

v-for基于数组渲染一个列表

 <li v-for="item in items">
  {{ item.message }}
</li>

事件处理

**1.内联事件处理器：事件被触发时执行的内联js语句**

const count = ref(0)

<button @click="count++">Add 1</button>

<p>Count is: {{ count }}</p>

**2.方法·事件处理器：一个指向组件上定义的方法的属性名或者路径**

.passive修饰符一般用于触摸事件的监听器，可以用来改善移动端设备的滚屏功能

