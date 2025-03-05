<script>
let { text = "MenuItem Text", href = "#", selected = false, extraClass } = $props();
</script>

<a href={href} class={["p-2 transition-all ease-in-out duration-300", !selected && "hover:px-4 hover:bg-neutral-600 active:bg-neutral-700", selected && "px-4 bg-green-700", extraClass]}>{text}</a>

