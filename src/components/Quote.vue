<template>
<div class="quote">
    <div class="title quote">
        <slot name="title"></slot>
        <span style="color: green"><slot name="subtitle">The Subtitle</slot></span>
    </div>
    <div class="quote">
        <slot ></slot>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style>
.quote {
        border: 1px solid #ccc;
        box-shadow: 1px 1px 2px black;
        padding: 30px;
        margin: 30px auto;
        text-align: center;
    }

    h2 {
        color: red;
    }

    .title {
        font-style: italic;
    }
</style>
