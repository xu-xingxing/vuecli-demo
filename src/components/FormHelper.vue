<template>
	<div id="form-helper">
		<h1>填充以下表单内容</h1>
		<div id="form-header">
			<slot name="form-header"></slot>
		</div>
		<div id="form-fields">
			<slot name="form-fields"></slot>
		</div>
		<div id="form-controls">
			<slot name="form-controls"></slot>
		</div>
		<div id="form-links">
			<ul>
				<li>
					<a href="#">link 1</a>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
  name: 'FormHelper',
	data() {
		return {}
	}
}
</script>

<style scoped>
</style>
