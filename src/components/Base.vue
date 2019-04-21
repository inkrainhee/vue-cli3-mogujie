<template>
    <div id="base-temp">
        <div id="base-header">
            <slot name="header">Submit</slot>
        </div>
        <div id="base-body">
            <slot name="body">Submit</slot>
        </div>
        <div id="base-footer">
            <slot name="footer">Submit</slot>
        </div>
    </div>
</template>

<script>
export default {
    name:'base-temp'
}
</script>

<style lang="stylus" scoped>
#base-header
    width :100%;
#base-body
    width :100%;
#base-footer
    width :100%;
    

</style>
