<template>
<div class="pdf" >
    <p class="arrow">
    <span @click="changePdfPage(0)" class="turn" :class="{grey: currentPage==1}">Preview</span>
    {{currentPage}} / {{pageCount}}
    <span
        @click="changePdfPage(1)"
        class="turn"
        :class="{grey: currentPage==pageCount}"
    >Next</span>
    </p>
    <!-- 自己引入就可以使用,这里我的需求是做了分页功能,如果不需要分页功能,只要src就可以了 -->
    <!-- // src需要展示的PDF地址 // 当前展示的PDF页码// PDF文件总页码// 一开始加载的页面// 加载事件 -->
    <pdf
    :src="src"
    :page="currentPage"
    @num-pages="pageCount=$event"
    @page-loaded="currentPage=$event"
    
    ></pdf>
</div><!-- @loaded="loadPdfHandler" -->
</template>
<script>
import pdf from 'vue-pdf'
export default {
components: {pdf},
data () {
return {
    currentPage: 1, 
    pageCount: 0, 
    fileType: 'pdf', 
    src: './pdfFiles/demopoem.pdf'
    }
},
// created: {
// // 有时PDF文件地址会出现跨域的情况,这里最好处理一下
//     this.src = pdf.createLoadingTask(this.src)
// }
methods: {
      // 改变PDF页码,val传过来区分上一页下一页的值,0上一页,1下一页
    changePdfPage (val) {
        console.log(val)
        if (val === 0 && this.currentPage > 1) {
        this.currentPage--
        console.log(this.currentPage)
        }
        if ( val === 1 && this.currentPage < this.pageCount){
        this.currentPage++
        console.log(this.currentPage)
        }
    }
}
}
</script>