<template>
    <i
        :class="`material-icons ${addClass ? addClass : ''}`"
        @mouseover="isActive ? isActive = !isActive : ''"
        @mouseout="active !== '' && !isActive ? isActive = !isActive : ''">

        {{ isActive ? 'favorite_border' : 'favorite' }}
    </i>
</template>

<script type="text/javascript">
    export default {
        props: [
            'active',
            'addClass',
        ],

        data: function () {
            return {
                isActive: this.active,
            }
        }
    }
</script>