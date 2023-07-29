<script setup>
</script>

<template>
    <div class="border-black bg-[url(/img/bg.png)] bg-center bg-cover min-h-[100vh]" id="home">
        <div class="bg-gradient-to-t from-[#fff] to-[#fff3] px-3 backdrop-blur-[1px] h-[100vh] text-gray-800">
            <div class="flex justify-center h-[100vh]">
                <div class="m-auto">
                    <slot name="title"></slot>
                    <slot name="text"></slot>
                    <slot name="body"></slot>
                </div>
            </div>
        </div>
    </div>
</template>