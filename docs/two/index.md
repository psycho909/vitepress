# Two index

<script setup>
import {ref} from "vue";
import {useData} from "vitepress";

const {page}=useData();
const count=ref(0);

const handleClick=()=>{
    count.value++;
}
</script>

::: v-pre
`{{ This will be displayed as-is }}`
:::

```html
<ul>
	<li v-for="todo in todos" :key="todo.id">{{ todo.text }}</li>
</ul>
```

<pre>{{page}}</pre>
<div class="box" @click="handleClick">BOX {{count}}</div>

<style>
    .box{
        width: 100px;
        height: 100px;
        border:1px solid #000;
    }
</style>
