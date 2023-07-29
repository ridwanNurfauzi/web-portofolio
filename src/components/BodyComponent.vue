<script>
export default {
    props: ['biodata', 'skill', 'project']
}
</script>

<template>
    <div class="bg-white flex flex-col pb-7 gap-x-3" id="bio">
        <div class="flex flex-wrap justify-center pt-7 container mx-auto">
            <div class="pt-7 flex mx-4">
                <div class="mx-3 max-w-max overflow-hidden rounded-xl hover:shadow-lg transition">
                    <img class="hover:scale-125 transition-all hover:opacity-75" src="/img/kkrdwn2.jpg" alt="KKRDWN_"
                        width="300">
                </div>
            </div>
            <div class="pt-7 flex mx-4">
                <div class="mx-auto my-auto">
                    <h2 class="text-center font-semibold text-2xl my-2">Biodata</h2>
                    <table class="mx-auto">
                        <tr v-for="data in biodata">
                            <td class="px-1">{{ data[0] }}</td>
                            <td class="px-1">:</td>
                            <td class="px-1">{{ data[1] }}</td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
        <div class="flex flex-wrap justify-center pb-7 container mx-auto">
            <div class="pt-7 container">
                <div class="mx-3 w-auto my-auto">
                    <h2 class="text-center font-semibold text-2xl my-2">Keterampilan</h2>
                    <div class="flex flex-wrap items-center justify-center">
                        <div class="flex" v-for="(data, i) in skill">
                            <div
                                class="shadow-sm p-2 m-2 rounded-lg hover:shadow-md hover:scale-125 hover:opacity-80 transition-all bg-gray-600 text-white cursor-default">
                                <h3>{{ data }}</h3>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="bg-gray-200 px-3 py-3" id="project">
        <h2 class="font-semibold text-2xl text-center mt-5">My Project</h2>
        <div class="flex">
            <div class="flex flex-wrap m-9 mx-auto justify-center">
                <div v-for="proj in project" class="mx-4">
                    <a class="m-5" target="_blank" v-bind:href="proj.link">
                        <div
                            class="w-[300px] h-[120px] hover:opacity-75 hover:scale-110 transition bg-white hover:shadow-md rounded-md flex items-center">
                            <div class="w-[65px] h-[65px]  mx-4 bg-center bg-cover">
                                <img v-bind:src="proj.iconUrl" v-bind:alt="''" class="w-[100%]">
                            </div>
                            <h2 class="font-semibold text-lg">{{ proj.title }}</h2>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>