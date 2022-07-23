
```vue
<script setup lang="ts">
import { ref, onBeforeMount }
const customElement = ref();
onBeforeMount( () => {
	console.log(customElement.value.el.innerHTML);
})
</script>

<template>
	<popup-content v-show="false" ref="customElement"></popup-content>
<template>
```

