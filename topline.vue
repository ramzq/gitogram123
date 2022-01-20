<template>
    <div class="c-topline">
        <div class="x-conainer">
            <div class="headline">
                <slot name="headline" />
            </div>
            <div class="content" v-if="$slots.content">
                <slot name="content" />
            </div>
        </div>
    </div>

</template>
