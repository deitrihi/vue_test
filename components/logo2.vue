<template>
    <div>777{{ status }}888</div>
</template>

<script>
export default {
    async asyncData () {
        const { data } = await axios.get('https://oasisapi.nexon.com/game/alllist')
        return { status: data.status }
        // return axios.get('https://oasisapi.nexon.com/game/alllist')
        // .then((res) => { 
        //     return { st : res.data.status }
        // })
        // .catch((e) => {
        //     return  { st : 500 }
        // })
    }
}
</script>