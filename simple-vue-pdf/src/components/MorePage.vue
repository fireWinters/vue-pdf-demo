<template>
	<div>
		<pdf
			v-for="i in numPages"
			:key="i"
			:src="src"
			:page="i"
			style="display: inline-block; width: 25%"
		></pdf>
	</div>
</template>

<script>

import pdf from 'vue-pdf'

var loadingTask = pdf.createLoadingTask('./pdfFiles/JavaScript高级程序设计（第3版）非扫描版.pdf');

export default {
	components: {
		pdf
	},
	data() {
		return {
			src: loadingTask,
			numPages: undefined,
		}
	},
	mounted() {

		this.src.then(pdf => {

			this.numPages = pdf.numPages;
		});
	}
}

</script>