<template>
    <div class="the-card">
        <div class="the-card__title">
            {{CardTitle}}
        </div>
        <div class="the-card__body">
            <slot>There have no slots value</slot>
        </div>
    </div>
  
</template>

<script>
export default {
    props: ["CardTitle"]

}
</script>

<style>
.the-card{
    width:200px;
    border: 1px solid #006f88;
    min-height: 200px;
    margin:22px;
}
.the-card__title{
    background: #167db1;
    padding:5px 11px;
    color:#fff;
}
.the-card__body{
    padding: 11px;

}
.the-card__body img{
    height: 111px;
}

</style>