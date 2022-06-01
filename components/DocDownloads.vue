<template>
<div>
    <h5 class="text-center text-lg">Download Documents</h5>
    <div class="flex gap-2 justify-center flex-wrap flex-col">
    <div v-for="doc in documents" :key="`${doc.id}-docs`" class="p-1
    ">
        <a :href="doc.file" download class="text-sm cursor-pointer">📄 {{ doc.name }}</a>
    </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            documents: [
                {
                    id: 0,
                    name: "Prospectus",
                    file: "/New Prospectus 2022.docx"
                },
                {
                    id: 1,
                    name: "Disciplinary Policy",
                    file: "/DISCIPLINARY POLICY 2022.docx"
                },
                {
                    id: 2,
                    name: "Internet Consent Form",
                    file: "/New Internet Consent Form 2022.docx"
                },
                {
                    id: 3,
                    name: "Medical Disclaimer",
                    file: "New Medical Disclaimer Form 2022 .docx",
                }
            ]
        }
    },
}
</script>