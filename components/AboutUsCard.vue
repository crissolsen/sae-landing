<template>
<div>
    
    <div>
        {{ text }}
    </div>
</div>

</template>

<script>
export default {
    props: {
        text: {
            type: String,
        },
        image: {
            type: String
        }
    },
}
</script>