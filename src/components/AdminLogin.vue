<template>
  <section class="auth-section">
    <div class="auth-card">
      <h2 class="auth-title">Admin Login</h2>
      <form @submit.prevent="handleLogin" class="auth-form">
        <div class="form-group">
          <label for="username">Username</label>
          <input type="text" id="username" v-model="username" required placeholder="Enter admin username" />
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input type="password" id="password" v-model="password" required placeholder="Enter admin password" />
        </div>
        <div v-if="error" class="auth-error">{{ error }}</div>
        <button type="submit" class="auth-btn" :disabled="loading">
          <span v-if="!loading">Login</span>
          <span v-else>Logging in...</span>
        </button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AdminLogin',
  data() {
    return {
      username: '',
      password: '',
      error: '',
      loading: false,
    }
  },
  methods: {
    handleLogin() {
      this.error = ''
      if (!this.username || !this.password) {
        this.error = 'Please enter both username and password.'
        return
      }
      
      this.loading = true
      
      // Simple admin authentication (in real app, this would be server-side)
      setTimeout(() => {
        this.loading = false
        
        // Check admin credentials (demo: admin/admin123)
        if (this.username === 'admin' && this.password === 'admin123') {
          localStorage.setItem('cryptoharvest_admin', 'true')
          this.$router.push('/admin')
        } else {
          this.error = 'Invalid admin credentials.'
        }
      }, 1000)
    },
  },
}
</script>

<style scoped>
.auth-section {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(120deg, #eb6709 0%, #f63d43 100%);
}

.auth-card {
  background: #202020;
  padding: 48px 32px 32px 32px;
  border-radius: 18px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.18);
  width: 100%;
  max-width: 400px;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.auth-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 24px;
  background: linear-gradient(90deg, #eb6709 0%, #f63d43 100%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  text-align: center;
}

.auth-form {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.form-group {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

label {
  margin-bottom: 6px;
  font-size: 1rem;
  color: #ffa600;
  font-weight: 600;
}

input {
  width: 100%;
  padding: 12px 14px;
  border-radius: 8px;
  border: none;
  background: #181818;
  color: #fff;
  font-size: 1rem;
  outline: none;
  margin-bottom: 2px;
}

input:focus {
  border: 1.5px solid #eb6709;
}

.auth-btn {
  width: 100%;
  padding: 12px 0;
  border-radius: 8px;
  background: linear-gradient(90deg, #eb6709 0%, #f63d43 100%);
  color: #fff;
  font-size: 1.1rem;
  font-weight: 700;
  border: none;
  cursor: pointer;
  margin-top: 8px;
  transition: background 0.3s, color 0.3s;
}

.auth-btn:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.auth-btn:hover:not(:disabled) {
  background: #fff;
  color: #eb6709;
}

.auth-error {
  color: #f63d43;
  font-size: 0.98rem;
  margin-bottom: 2px;
  text-align: left;
}

@media (max-width: 600px) {
  .auth-section {
    padding: 30px 20px;
  }

  .auth-card {
    padding: 24px 8px 18px 8px;
    border-radius: 10px;
  }

  .auth-title {
    font-size: 1.2rem;
  }
}
</style> 