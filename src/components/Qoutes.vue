<template>
	<section class="row qoutes">
		<div class="col-xs-8 qoutes-wrapper">
			<ul>
				<li v-for="(qoute, index) in qoutes" :key="index">
					<div class="qoute-wrapper" @click="deleteQoute(index)">
						{{ qoute}}
					</div>
				</li>
			</ul>
		</div>
	</section>
</template>

<script>
export default {
  props: {
		qoutes: Array,
		deleteQoute: Function
  }
};
</script>

<style lang="scss" scoped>
.qoutes {
  margin: 50px auto 40px auto;
  .qoutes-wrapper {
    padding: 0px;
    ul {
      margin: 0 auto;
      padding-left: 0px;
      .qoute-wrapper {
        cursor: pointer;
      }
      li {
        font-family: "Merienda", cursive;
        display: inline-block;
        margin: 0px 30px 20px 0px;
				padding: 20px 10px;
        border: 1px solid transparent;
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12),
          0 6px 6px rgba(0, 0, 0, 0.23);
      }
    }
  }
}
</style>
