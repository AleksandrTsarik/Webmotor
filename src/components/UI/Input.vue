<template>

    <div v-if="type === 'text'" class="block-input">
        <label>
            <input 
                type="text"
                :value="value"
                :placeholder="placeholder"
            >
            <span v-if="name">{{ name }}</span>
        </label>
    </div>

    <div v-else-if="type === 'tel'" class="block-input">
        <label>
            <MaskInput type="tel"  v-model="phoneNumber" mask="+7(###) ###-##-##" placeholder="+7 (-&#45;&#45;) -&#45;&#45; &#45;&#45; &#45;&#45;" />
            <span v-if="name">{{ name }}</span>
        </label>
    </div>
    <div v-else-if="type === 'email'" class="block-input">
        <label>
            <input 
                :value="value" 
                type="email" 
                :placeholder="placeholder"
            >
            <span v-if="name">{{ name }}</span>
        </label>
    </div>
</template>

<script>
import { MaskInput } from 'vue-3-mask';
export default {
    components: {
        MaskInput
    },
    props: {
        value: {
            type: [String, Number],
            default: ''
        },
        label: {
            type: String,
            default: ''
        },
        name: {
            type: String,
            default: ''
        },
        type: {
            type: String,
            defrault: '',
            require: true
        },
        placeholder: {
            type: String,
            default: '',
            require: true
        }
    },
}
</script>

<style lang="scss">
.block-input {
    width: 100%;
    border: solid 1px transparent;
    border-radius: 10px;
    font-size: 14px;
    position: relative;
    margin-bottom: 10px;
    background-color: var(--bg);
    input {
        padding: 15px 16px;
        width: 100%;
        text-overflow: ellipsis;
        &::placeholder {
            color: var(--placeholder);
        }
    }
}
</style>