<template>
    <div id="base-header">
        <slot name="header">Submit</slot>
    </div>
</template>

<script>
export default {
    name:'base-header'
}
</script>

<style lang="stylus" scoped>
#base-header
    width :100%;
</style>
