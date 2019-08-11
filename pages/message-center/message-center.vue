<template>
	<view class="container">
		<top-tab-bar 
		:tabNames="tabNames"
		:showSlider="true"
		@onTabClick="onTabClick">
		</top-tab-bar>
		<message-list class="list" :messages="currentMessages"></message-list>
	</view>
</template>

<script>
	import TopTabBar from "./top-tab-bar.vue"
	import messageData from "./message-data.js"
	import MessageList from "./message-list.vue"
	
	export default {
		components: {
			TopTabBar,
			MessageList
		},
		data() {
			return {
				tabNames: ["代办","已办","待阅","已阅"],
				messages: [messageData.todo, messageData.done, messageData.unread, messageData.readed],
				currentMessages: messageData.todo
			}
		},
		methods: {
			onTabClick(index) {
				console.log("parent receive on tab click! ");
				this.$data.currentMessages = this.$data.messages[index];
			}
		}
	}
</script>

<style scoped>

</style>
