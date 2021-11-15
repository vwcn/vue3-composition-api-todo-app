<template>
	<h1>ToDo App</h1>
	<form @submit.prevent="addTodo()">
		<label>New ToDo </label>
		<input
			:value="task"
			name="task"
			autocomplete="off"
		>
		<button>Add ToDo</button>
	</form>
	<h2>ToDo List</h2>
	<ul>
		<li
			v-for="(todo, index) in todos"
			:key="index"
		>
			<span
				:class="{ done: todo.done }"
				@click="toggleTodo(todo)"
			>{{ todo.content }}</span>
			<button @click="removeTodo(index)">Remove</button>
		</li>
	</ul>
	<h4 v-if="todos.length === 0">Empty list.</h4>
</template>

<script setup>
	import { ref, reactive } from 'vue';
	const task = ref(null)
	const todos = reactive([])

	const addTodo = ()=> {

	}
	const toggleTodo = ()=> {

	}
	
</script>

<style>
</style>
