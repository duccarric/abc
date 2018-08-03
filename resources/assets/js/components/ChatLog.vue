<template lang="html">
    <div class="chat-log">
        <chat-message v-for="message in messages" :message="message"></chat-message>
        <chat-composer @messagesent="sent"></chat-composer>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                messages:[
                    {
                        message: 'Hey!',
                        user: "John Doe"
                    },
                    {
                        message: 'Hello!',
                        user: "John Doe"
                    }
                ]
            }

        },
        methos:{
            sent() {
                console.log('ok');
            }
        }
    }
</script>

<style lang="css">

</style>
.chat-log .chat-message:nth-child(even){
backround-color: #ccc;
}