<template>
  <!-- investing-section -->
  <div class="investing-section animate-fade-slide">
    <h1>Start investing with CryptoHarvest investment</h1>

    <!-- investing-cards-->
    <div class="investing-cards">
      <template v-for="(card, idx) in cards" :key="idx">
        <div class="investing-card animate-fade-slide">
          <h2>{{ idx + 1 }}</h2>
          <!-- card-text -->
          <div class="card-text">
            <h3>{{ card.title }}</h3>
            <p>{{ card.text }}</p>
          </div>
        </div>
        <div v-if="idx < cards.length - 1" class="card-divider"></div>
      </template>
    </div>
  </div>
  <Questions />
  <Customer />
</template>

<script>
import Customer from './Customer.vue'
import Questions from './Questions.vue'

export default {
  name: 'Investing',
  components: {
    Customer,
    Questions,
  },
  data() {
    return {
      cards: [
        {
          title: 'Create an account',
          text: `Get started on your investment journey by signing up for an account in just a few simple steps. Provide your details, verify your identity, and unlock access to a world of investment opportunities. With our secure and user-friendly platform, you're just moments away from growing your wealth with confidence.`,
        },
        {
          title: 'Fund your account',
          text: `Easily deposit funds using a variety of secure payment methods. Your money is protected with industry-leading security protocols, ensuring a safe and seamless funding experience.`,
        },
        {
          title: 'Start investing',
          text: `Explore a wide range of investment options tailored to your goals. Track your progress, manage your portfolio, and watch your wealth grow with our intuitive tools and expert support.`,
        },
      ],
    }
  },
}
</script>

<style scoped>
.investing-section {
  background: #202020;
  padding: 40px 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.investing-section h1 {
  color: #eb6709;
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 36px;
  text-transform: uppercase;
  text-align: center;
  letter-spacing: 0.5px;
}

.investing-cards {
  display: flex;
  flex-direction: row;
  gap: 24px;
  justify-content: center;
  padding: 20px 60px;
  align-items: stretch;
  flex-wrap: wrap;
}

.investing-card {
  background: #181818;
  border-radius: 18px;
  box-shadow:
    0 4px 24px rgba(0, 0, 0, 0.12),
    0 1.5px 6px rgba(235, 103, 9, 0.08);
  padding: 36px 28px 32px 28px;
  min-width: 280px;
  max-width: 340px;
  flex: 1 1 300px;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition:
    transform 0.2s,
    box-shadow 0.2s;
  position: relative;
}

.investing-card h2 {
  background: linear-gradient(90deg, #eb6709 0%, #f63d43 100%);
  color: #fff;
  border-radius: 50%;
  width: 54px;
  height: 54px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  font-weight: 800;
  margin-bottom: 18px;
  box-shadow: 0 2px 8px rgba(235, 103, 9, 0.12);
}

.card-text h3 {
  color: #eb6709;
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 10px;
  text-align: center;
}

.card-text p {
  color: #e9e9e9;
  font-size: 1rem;
  line-height: 1.6;
  text-align: center;
}

.card-divider {
  width: 2px;
  height: 80px;
  background: #ccc;
  align-self: center;
  margin: 0 18px;
  border-radius: 2px;
}

.investing-card:hover {
  transform: translateY(-8px) scale(1.04);
  box-shadow:
    0 8px 32px rgba(235, 103, 9, 0.12),
    0 2px 12px rgba(0, 0, 0, 0.1);
}

.animate-fade-slide {
  opacity: 0;
  transform: translateY(40px);
  animation: fadeSlideUp 0.8s cubic-bezier(0.4, 0, 0.2, 1) 0.1s forwards;
}
@keyframes fadeSlideUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 900px) {
  .investing-cards {
    flex-direction: column;
    align-items: center;
    gap: 18px;
    width: 100%;
    padding: 20px 30px;
  }

  .card-divider {
    width: 80px;
    height: 2px;
    margin: 18px 0;
  }
}

@media (max-width: 600px) {
  .investing-section {
    padding: 20px 16px;
  }

  .investing-section h1 {
    font-size: 1.2rem;
    margin-bottom: 18px;
  }

  .investing-card {
    padding: 18px 8px 16px 8px;
    min-width: 0;
    max-width: 100%;
  }

  .investing-card h2 {
    width: 38px;
    height: 38px;
    font-size: 1.2rem;
    margin-bottom: 10px;
  }

  .card-text h3 {
    font-size: 1rem;
    margin-bottom: 6px;
  }

  .card-text p {
    font-size: 0.92rem;
  }

  .card-divider {
    width: 40px;
    height: 2px;
    margin: 8px 0;
  }
}
</style>
