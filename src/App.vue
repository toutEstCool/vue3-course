<template>
	<div class="app">
		<form class="form">
			<h4>Создание поста</h4>
			<input
				v-bind:value="title"
				class="input"
				type="text"
				placeholder="Заголовок поста..."
			/>
			<input
				v-bind:value="body"
				class="input"
				type="text"
				placeholder="Описание поста..."
			/>
			<button class="btn">Отправить</button>
		</form>
		<div class="post" v-for="post in posts">
			<div><strong>Название:</strong> {{ post.title }}</div>
			<div><strong>Описание:</strong> {{ post.body }}</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			posts: [
				{ id: 1, title: 'JavaScript', body: 'Пост о функциях в JS' },
				{ id: 2, title: 'TypeScript', body: 'Анбординг сотрудников' },
				{ id: 3, title: 'Vue', body: 'Чем же он так хорошь ?' },
			],
			title: '',
			body: '',
		}
	},

	methods: {
		createPost() {},
	},
}
</script>

<style>
* {
	padding: 0;
	margin: 0;
	box-sizing: border-box;
	font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.app {
	max-width: 1200px;
	margin: 0 auto;
	padding: 0 20px;
}

.post {
	padding: 10px;
	margin-top: 10px;
	border-radius: 5px;
	border: 1px solid #3fb883;
}

.form {
	width: 100%;
	display: flex;
	flex-direction: column;
}

.input {
	width: 100%;
	padding: 5px 10px;
	margin-top: 10px;
}

.btn {
	align-self: flex-end;
	margin-top: 10px;
	padding: 8px 16px;
	cursor: pointer;
	background: #3fb883;
	border: none;
	color: whitesmoke;
	border-radius: 5px;
}
</style>
