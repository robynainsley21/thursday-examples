<template>
  <div>
    <div class="container">
      <div class="row">
        <UserDetail firstName="Robyn" lastName="Carnow" title="Software Developer" />
        <UserDetail firstName="Robyn" lastName="Carnow" title="Software Developer" />
      </div>
      <div class="row">
        <h2>App component</h2>
      </div>
      <div class="row">
        <Card v-for="(friend, index) in friends" :key="index">
          <template #cardHeader>
            <img src="friend.profile" alt="friend.firstname" loading="lazy">
          </template>
          <template #cardBody>
            <p>{{ friend.firstName }} {{ friend.lastName }}</p>
          </template>
        </Card>
      </div>
    </div>
  </div>
</template>

<script>
import UserDetail from '@/components/UserDetails.vue'
import Card from '@/components/Card.vue'

export default {
  name: 'App',
  data() {
    return {
      friends: [
        {
          firstName: "Joel",
          lastName: "Mukanya",
          profile: "https://robynainsley21.github.io/images/profile-Image.png"
        },
        {
          firstName: "Jane",
          lastName: "Doe",
          profile: "https://robynainsley21.github.io/images/profile-Image.png"
        },
        {
          firstName: "John",
          lastName: "Doe",
          profile: "https://robynainsley21.github.io/images/profile-Image.png"
        }
      ]
    }
  },
  components: {
    UserDetail,
    Card
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
