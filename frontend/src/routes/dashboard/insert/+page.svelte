<div class="m-auto w-[60%] flex flex-col gap-4">
	<h1 class="text-center text-3xl font-bold">Insert New Entry</h1>
	<form class="grid grid-cols-8 gap-2 items-center">
		<label for="name">Name</label>
		<input id="name" type="text" placeholder="Item's name"
			class="col-span-7" />

		<label for="type">Type</label>
		<select class="col-span-3">
			<option>Type 1</option>
			<option>Type 2</option>
		</select>

		<label for="quantity">Quantity</label>
		<input id="quantity" type="number" value="1" min="1"
			class="col-span-3" />

		<label for="description">Description</label>
		<textarea id="description" placeholder="Item's description"
			class="col-span-7"></textarea>
		
		<label for="image">Upload Image</label>
		<input id="image" type="file" class="hidden" />
		<div class="form-input px-2 col-span-7 rounded-md flex flex-wrap gap-1">
			<!--<img alt="images" class="size-24 px-1 border-1 rounded-sm" />-->
			<button>Add Image...</button>
		</div>

		<button class="col-span-8">Insert</button>
	</form>
</div>
