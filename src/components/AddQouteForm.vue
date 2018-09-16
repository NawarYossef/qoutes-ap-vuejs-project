<template>
	<form action="/" method="">
		<div>
			<label for="comments">
				<h5>New Qoute</h5>
				<textarea rows="4" cols="50" name="qoute" @change="e => this.$emit('input', e.target.value)">
				</textarea>
			</label>
		</div>
		<button type="submit" value="Submit" @click.prevent="handleSubmit()">Add Qoute</button>
	</form>
</template>

<script>
export default {
  props: {
    newQoute: String,
    handleSubmit: Function
  }
};
</script>

<style lang="scss" scoped>
.form {
  text-align: center;
	textarea {
		font-family: sans-serif;
		font-weight: 100;
	}
}
</style>
