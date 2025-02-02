<template>
    <div class="w-full">
        <checkbox-field
            :field="field"
            :resource-name="resourceName"
            :resource-id="resourceId"
            :field-value="value"
            @input="value => $emit('input', value)"
        />
    </div>
</template>

<script>
export default {
    props: {
        field: {
            type: Object,
            required: true,
        },
        resourceName: {
            type: String,
            required: true,
        },
        resourceId: {
            type: [Number, String],
        },
        value: {
            type: Boolean,
            default: false,
        },
    },
}
</script> 