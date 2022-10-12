<!-- Iteración 1: pasar el contenido del primer Tweet como prop -->
<!-- <template>
    <div class="tweet">
        <img :src="props.infoTweet.user.image" class="profile" alt="profile" />

        <div class="body">
            <div class="top">
                <span class="user">
                    <span class="name">{{ props.infoTweet.user.name }}</span>
                    <span class="handle">{{ props.infoTweet.user.handle }}</span>
                </span>

                <span class="timestamp">{{ props.infoTweet.timestamp }}</span>
            </div>

            <p class="message">
                {{ props.infoTweet.message }}
            </p>

            <div class="actions">
                <i class="far fa-comment"></i>
                <i class="fas fa-retweet"></i>
                <i class="far fa-heart"></i>
                <i class="fas fa-share"></i>
            </div>
        </div>

        <i class="fas fa-ellipsis-h"></i>
    </div>
</template>
-->

<template>
    <div class="tweet">
        <ProfileImage :image="props.infoTweet.user.image" />

        <div class="body">
            <div class="top">
                <User :userData="props.infoTweet.user" />
                <Timestamp :time="props.infoTweet.timestamp" />
            </div>

            <Message :message="props.infoTweet.message" />
            <Actions />
        </div>

        <i class="fas fa-ellipsis-h"></i>
    </div>
</template>

<script setup>
import { defineProps } from "vue";
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

// const props = defineProps(["infoTweet"])
const props = defineProps({
    infoTweet: {
        type: Object,
        required: true,
        default: "missing data",
    },
});
</script>

<style scoped>
a {
    color: #42b983;
}
</style>
