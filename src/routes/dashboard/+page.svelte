<script>
	import Todoform from '../../components/dashboard/Todoform.svelte';
	import TodoList from '../../components/dashboard/TodoList.svelte';

	//state
	let todoInput = '';
	let todoList = [
		{
			text: 'Buy more oatmilk',
			status: true
		},
		{
			text: 'Fold laundry',
			status: false
		}
	];
	function addToList() {
		todoList = [{ text: todoInput, status: true }, ...todoList];
	}
</script>

<div class="h-screen">
	<div class="flex min-h-full items-center justify-center py-12 px-4 sm:px-6 lg:px-8">
		<div class="w-full max-w-md space-y-16">
			<Todoform {todoInput} add={addToList} />
			<TodoList todos={todoList} />
		</div>
	</div>
</div>
