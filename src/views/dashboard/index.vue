<template>
  <div class="dashboard-container">
    <component :is="currentRole" />
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import userDashboard from './user'
import visitorDashboard from './visitor'

export default {
  name: 'Dashboard',
  components: { userDashboard, visitorDashboard },
  data() {
    return {
      currentRole: 'userDashboard'
    }
  },
  computed: {
    ...mapGetters([
      'roles'
    ])
  },
  created() {
    if (!this.roles.includes('admin')) {
      this.currentRole = 'visitorDashboard'
    }
  }
}
</script>
