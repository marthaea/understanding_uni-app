<template>
  <view class="page-container">
    <!-- Hero Section -->
    <view class="hero-section">
      <view class="hero-content">
        <view class="hero-left">
          <text class="company-name">webNexus</text>
          <text class="slogan">code, words, art</text>
          <view class="hero-description">
            <text
              >Fostering creativity and storytelling through technology in
              Kampala, Uganda</text
            >
          </view>
          <view class="cta-container">
            <button class="primary-btn cursor-pointer">Explore Our Work</button>
            <button class="secondary-btn cursor-pointer">Contact Us</button>
          </view>
        </view>
        <view class="hero-right">
          <image
            class="hero-image"
            src="https://readdy.ai/api/search-image?query=Abstract%20geometric%20patterns%20in%20purple%20and%20blue%2C%20digital%20creative%20technology%20concept%20art%2C%20flowing%20shapes%20and%20lines%2C%20futuristic%20design%20elements%2C%20clean%20modern%20aesthetic%2C%20high%20detail%20quality%2C%20dynamic%20composition%20with%20depth%2C%20tech%20inspired%20artwork&width=600&height=600&seq=hero01&orientation=squarish"
            mode="aspectFill"
          ></image>
        </view>
      </view>
      <view class="floating-elements">
        <view class="float-element float-1"></view>
        <view class="float-element float-2"></view>
        <view class="float-element float-3"></view>
      </view>
    </view>

    <!-- Services Section -->
    <view class="section-title-container">
      <text class="section-title">Our Services</text>
      <text class="section-subtitle"
        >Creative solutions for your digital needs</text
      >
    </view>

    <view class="services-grid">
      <view
        class="service-tile cursor-pointer"
        v-for="(service, index) in services"
        :key="index"
      >
        <view class="service-icon-container">
          <image
            class="service-icon"
            :src="service.iconUrl"
            mode="aspectFit"
          ></image>
        </view>
        <text class="service-name">{{ service.name }}</text>
        <text class="service-description">{{ service.description }}</text>
      </view>
    </view>

    <!-- Creative Storytelling Section -->
    <view class="storytelling-section">
      <view class="section-title-container">
        <text class="section-title">Our Creative Process</text>
        <text class="section-subtitle">Where technology meets creativity</text>
      </view>

      <view class="timeline-container">
        <view class="timeline-line"></view>
        <view class="timeline-steps">
          <view
            class="timeline-step"
            v-for="(step, index) in creativeProcess"
            :key="index"
          >
            <view class="timeline-dot"></view>
            <view class="timeline-content">
              <text class="timeline-step-number">{{ index + 1 }}</text>
              <text class="timeline-title">{{ step.title }}</text>
              <text class="timeline-description">{{ step.description }}</text>
            </view>
          </view>
        </view>
      </view>

      <view class="african-patterns">
        <image
          class="pattern-image"
          src="https://readdy.ai/api/search-image?query=Modern%20minimalist%20African%20pattern%20design%2C%20geometric%20shapes%2C%20purple%20and%20blue%20color%20palette%2C%20abstract%20cultural%20motifs%2C%20clean%20lines%2C%20contemporary%20interpretation%20of%20traditional%20patterns%2C%20subtle%20texture%2C%20elegant%20composition%2C%20digital%20art%20style&width=800&height=200&seq=pattern01&orientation=landscape"
          mode="aspectFill"
        ></image>
      </view>
    </view>

    <!-- Portfolio Showcase -->
    <view class="portfolio-section">
      <view class="section-title-container">
        <text class="section-title">Featured Projects</text>
        <text class="section-subtitle">Explore our recent work</text>
      </view>

      <scroll-view
        class="portfolio-scroll"
        scroll-x="true"
        show-scrollbar="false"
      >
        <view class="portfolio-container">
          <view
            class="portfolio-item cursor-pointer"
            v-for="(project, index) in portfolioProjects"
            :key="index"
          >
            <image
              class="portfolio-image"
              :src="project.imageUrl"
              mode="aspectFill"
            ></image>
            <view class="portfolio-overlay">
              <text class="portfolio-title">{{ project.title }}</text>
              <text class="portfolio-category">{{ project.category }}</text>
            </view>
          </view>
        </view>
      </scroll-view>
    </view>

    <!-- Location Section -->
    <view class="location-section">
      <view class="section-title-container">
        <text class="section-title">Find Us in Kampala</text>
        <text class="section-subtitle">Where innovation happens</text>
      </view>

      <view class="location-container">
        <view class="map-container">
          <image
            class="map-image"
            src="https://readdy.ai/api/search-image?query=Stylized%20map%20of%20Kampala%20Uganda%2C%20modern%20digital%20cartography%2C%20tech%20inspired%20design%2C%20minimalist%20city%20layout%2C%20purple%20and%20blue%20color%20scheme%2C%20abstract%20representation%20of%20streets%20and%20landmarks%2C%20clean%20geometric%20style&width=600&height=400&seq=map01&orientation=landscape"
            mode="aspectFill"
          ></image>
        </view>
        <view class="location-info">
          <view class="info-item">
            <uni-icons
              class="info-icon"
              type="location"
              size="24"
              color="#6C63FF"
            ></uni-icons>
            <text class="info-text"
              >Innovation Hub, Kampala Business District</text
            >
          </view>
          <view class="info-item">
            <uni-icons
              class="info-icon"
              type="phone"
              size="24"
              color="#6C63FF"
            ></uni-icons>
            <text class="info-text">+256 123 456 789</text>
          </view>
          <view class="info-item">
            <uni-icons
              class="info-icon"
              type="email"
              size="24"
              color="#6C63FF"
            ></uni-icons>
            <text class="info-text">hello@webnexus.com</text>
          </view>
          <view class="social-links">
            <view class="social-icon cursor-pointer">
              <uni-icons type="instagram" size="24" color="#6C63FF"></uni-icons>
            </view>
            <view class="social-icon cursor-pointer">
              <uni-icons type="twitter" size="24" color="#6C63FF"></uni-icons>
            </view>
            <view class="social-icon cursor-pointer">
              <uni-icons type="facebook" size="24" color="#6C63FF"></uni-icons>
            </view>
            <view class="social-icon cursor-pointer">
              <uni-icons type="linkedin" size="24" color="#6C63FF"></uni-icons>
            </view>
          </view>
        </view>
      </view>
    </view>

    <!-- Newsletter Section -->
    <view class="newsletter-section">
      <view class="newsletter-container">
        <text class="newsletter-title">Stay Updated</text>
        <text class="newsletter-description"
          >Subscribe to our newsletter for the latest updates and creative
          insights</text
        >
        <view class="newsletter-form">
          <input
            class="newsletter-input"
            type="text"
            placeholder="Enter your email"
          />
          <button class="newsletter-button cursor-pointer">Subscribe</button>
        </view>
      </view>
    </view>

    <!-- Footer -->
    <view class="footer">
      <view class="footer-top">
        <view class="footer-logo">
          <text class="footer-company-name">webNexus</text>
          <text class="footer-slogan">code, words, art</text>
        </view>
        <view class="footer-links">
          <view class="footer-column">
            <text class="footer-column-title">Services</text>
            <text class="footer-link cursor-pointer">Animation</text>
            <text class="footer-link cursor-pointer">Web Design</text>
            <text class="footer-link cursor-pointer">Poster Design</text>
            <text class="footer-link cursor-pointer">Logo Design</text>
            <text class="footer-link cursor-pointer">Storyboards</text>
          </view>
          <view class="footer-column">
            <text class="footer-column-title">Company</text>
            <text class="footer-link cursor-pointer">About Us</text>
            <text class="footer-link cursor-pointer">Our Team</text>
            <text class="footer-link cursor-pointer">Careers</text>
            <text class="footer-link cursor-pointer">Contact</text>
          </view>
          <view class="footer-column">
            <text class="footer-column-title">Resources</text>
            <text class="footer-link cursor-pointer">Blog</text>
            <text class="footer-link cursor-pointer">Portfolio</text>
            <text class="footer-link cursor-pointer">Testimonials</text>
            <text class="footer-link cursor-pointer">FAQ</text>
          </view>
        </view>
      </view>
      <view class="footer-bottom">
        <text class="copyright">© 2025 webNexus. All rights reserved.</text>
        <view class="footer-bottom-links">
          <text class="policy-link cursor-pointer">Privacy Policy</text>
          <text class="policy-link cursor-pointer">Terms of Service</text>
        </view>
      </view>
      <view class="cityscape-container">
        <image
          class="cityscape-image"
          src="https://readdy.ai/api/search-image?query=Minimalist%20Kampala%20skyline%20illustration%2C%20modern%20city%20silhouette%2C%20purple%20and%20blue%20gradient%2C%20digital%20art%20style%2C%20clean%20lines%2C%20contemporary%20urban%20landscape%2C%20simplified%20architectural%20elements%2C%20tech%20inspired%20design%20aesthetic&width=1200&height=200&seq=city01&orientation=landscape"
          mode="aspectFill"
        ></image>
      </view>
    </view>

    <!-- Sticky Header -->
    <view class="header" :class="{ 'header-scrolled': isScrolled }">
      <view class="header-container">
        <view class="header-logo">
          <text class="header-company-name">webNexus</text>
        </view>
        <view class="header-nav">
          <text class="nav-item cursor-pointer">Home</text>
          <text class="nav-item cursor-pointer">Services</text>
          <text class="nav-item cursor-pointer">Projects</text>
          <text class="nav-item cursor-pointer">About</text>
          <text class="nav-item cursor-pointer">Contact</text>
        </view>
        <view class="mobile-menu-btn cursor-pointer">
          <uni-icons type="bars" size="24" color="#ffffff"></uni-icons>
        </view>
      </view>
    </view>
  </view>
</template>

<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from "vue";

const isScrolled = ref(false);

const services = ref([
  {
    name: "Animation",
    description: "Bringing stories to life through motion and visual effects",
    iconUrl:
      "https://readdy.ai/api/search-image?query=icon%2C%203D%20cartoon%2C%20Animation%20film%20reel%2C%20subject%20fills%2080%20percent%20of%20frame%2C%20vibrant%20colors%20with%20soft%20gradients%2C%20minimalist%20design%2C%20smooth%20rounded%20shapes%2C%20subtle%20shading%2C%20no%20outlines%2C%20centered%20composition%2C%20isolated%20on%20white%20background%2C%20playful%20and%20friendly%20aesthetic%2C%20isometric%20perspective%2C%20high%20detail%20quality%2C%20clean%20and%20modern%20look%2C%20single%20object%20focus&width=200&height=200&seq=service01&orientation=squarish",
  },
  {
    name: "Web Design",
    description:
      "Creating responsive, user-friendly websites with modern aesthetics",
    iconUrl:
      "https://readdy.ai/api/search-image?query=icon%2C%203D%20cartoon%2C%20Computer%20monitor%20with%20web%20design%20layout%2C%20subject%20fills%2080%20percent%20of%20frame%2C%20vibrant%20colors%20with%20soft%20gradients%2C%20minimalist%20design%2C%20smooth%20rounded%20shapes%2C%20subtle%20shading%2C%20no%20outlines%2C%20centered%20composition%2C%20isolated%20on%20white%20background%2C%20playful%20and%20friendly%20aesthetic%2C%20isometric%20perspective%2C%20high%20detail%20quality%2C%20clean%20and%20modern%20look%2C%20single%20object%20focus&width=200&height=200&seq=service02&orientation=squarish",
  },
  {
    name: "Poster Design",
    description: "Eye-catching visual communication that captures attention",
    iconUrl:
      "https://readdy.ai/api/search-image?query=icon%2C%203D%20cartoon%2C%20Poster%20design%20mockup%2C%20subject%20fills%2080%20percent%20of%20frame%2C%20vibrant%20colors%20with%20soft%20gradients%2C%20minimalist%20design%2C%20smooth%20rounded%20shapes%2C%20subtle%20shading%2C%20no%20outlines%2C%20centered%20composition%2C%20isolated%20on%20white%20background%2C%20playful%20and%20friendly%20aesthetic%2C%20isometric%20perspective%2C%20high%20detail%20quality%2C%20clean%20and%20modern%20look%2C%20single%20object%20focus&width=200&height=200&seq=service03&orientation=squarish",
  },
  {
    name: "Logo Design",
    description: "Distinctive brand identities that stand out in the market",
    iconUrl:
      "https://readdy.ai/api/search-image?query=icon%2C%203D%20cartoon%2C%20Logo%20design%20concept%20with%20pen%20tool%2C%20subject%20fills%2080%20percent%20of%20frame%2C%20vibrant%20colors%20with%20soft%20gradients%2C%20minimalist%20design%2C%20smooth%20rounded%20shapes%2C%20subtle%20shading%2C%20no%20outlines%2C%20centered%20composition%2C%20isolated%20on%20white%20background%2C%20playful%20and%20friendly%20aesthetic%2C%20isometric%20perspective%2C%20high%20detail%20quality%2C%20clean%20and%20modern%20look%2C%20single%20object%20focus&width=200&height=200&seq=service04&orientation=squarish",
  },
  {
    name: "Storyboards",
    description: "Visual narratives that guide the storytelling process",
    iconUrl:
      "https://readdy.ai/api/search-image?query=icon%2C%203D%20cartoon%2C%20Storyboard%20panels%20with%20sketches%2C%20subject%20fills%2080%20percent%20of%20frame%2C%20vibrant%20colors%20with%20soft%20gradients%2C%20minimalist%20design%2C%20smooth%20rounded%20shapes%2C%20subtle%20shading%2C%20no%20outlines%2C%20centered%20composition%2C%20isolated%20on%20white%20background%2C%20playful%20and%20friendly%20aesthetic%2C%20isometric%20perspective%2C%20high%20detail%20quality%2C%20clean%20and%20modern%20look%2C%20single%20object%20focus&width=200&height=200&seq=service05&orientation=squarish",
  },
]);

const creativeProcess = ref([
  {
    title: "Discovery",
    description:
      "We explore your vision, goals, and target audience to understand the core of your project.",
  },
  {
    title: "Concept Development",
    description:
      "Creative ideas are born through brainstorming, sketching, and collaborative thinking.",
  },
  {
    title: "Design & Creation",
    description:
      "Transforming concepts into visual realities with attention to detail and artistic excellence.",
  },
  {
    title: "Refinement",
    description:
      "Polishing every element to perfection through feedback and iterative improvements.",
  },
  {
    title: "Delivery",
    description:
      "Presenting the final product with comprehensive support and implementation guidance.",
  },
]);

const portfolioProjects = ref([
  {
    title: "Kampala Stories Animation Series",
    category: "Animation",
    imageUrl:
      "https://readdy.ai/api/search-image?query=Stylized%20animation%20scene%20of%20Kampala%20city%20life%2C%20vibrant%20colors%2C%20modern%20digital%20art%20style%2C%20storytelling%20visual%2C%20character%20designs%2C%20cultural%20elements%2C%20high%20quality%20render%2C%20artistic%20composition%20with%20depth&width=500&height=350&seq=portfolio01&orientation=landscape",
  },
  {
    title: "Tech Startup Website Redesign",
    category: "Web Design",
    imageUrl:
      "https://readdy.ai/api/search-image?query=Modern%20website%20design%20mockup%2C%20purple%20and%20blue%20color%20scheme%2C%20clean%20interface%2C%20responsive%20layout%20visualization%2C%20digital%20product%20presentation%2C%20tech%20aesthetic%2C%20high%20quality%20render&width=500&height=350&seq=portfolio02&orientation=landscape",
  },
  {
    title: "Cultural Festival Poster Series",
    category: "Poster Design",
    imageUrl:
      "https://readdy.ai/api/search-image?query=Artistic%20poster%20design%20for%20African%20cultural%20festival%2C%20vibrant%20colors%2C%20modern%20typography%2C%20geometric%20patterns%2C%20digital%20illustration%20style%2C%20purple%20and%20blue%20color%20palette%2C%20high%20quality%20render&width=500&height=350&seq=portfolio03&orientation=landscape",
  },
  {
    title: "Innovation Hub Brand Identity",
    category: "Logo Design",
    imageUrl:
      "https://readdy.ai/api/search-image?query=Modern%20logo%20design%20presentation%2C%20brand%20identity%20mockup%2C%20purple%20and%20blue%20color%20scheme%2C%20minimalist%20geometric%20style%2C%20digital%20presentation%20format%2C%20clean%20background%2C%20high%20quality%20render&width=500&height=350&seq=portfolio04&orientation=landscape",
  },
  {
    title: "Tech Education Storyboard",
    category: "Storyboards",
    imageUrl:
      "https://readdy.ai/api/search-image?query=Digital%20storyboard%20panels%2C%20educational%20technology%20narrative%2C%20sequential%20art%2C%20planning%20visualization%2C%20purple%20and%20blue%20color%20scheme%2C%20modern%20illustration%20style%2C%20high%20quality%20render&width=500&height=350&seq=portfolio05&orientation=landscape",
  },
]);

const handleScroll = () => {
  if (typeof window !== "undefined") {
    isScrolled.value = window.pageYOffset > 50;
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<style>
page {
  height: 100%;
}

/* Global Styles */
.page-container {
  width: 750rpx;
  min-height: 100%;
  font-family: "Arial", sans-serif;
  color: #333333;
  position: relative;
}

.cursor-pointer {
  cursor: pointer;
}

/* Header Styles */
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 750rpx;
  height: 100rpx;
  z-index: 1000;
  transition: all 0.3s ease;
  background-color: rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
}

.header-scrolled {
  background-color: rgba(53, 25, 104, 0.95);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 40rpx;
  height: 100%;
}

.header-company-name {
  font-size: 36px;
  font-weight: 700;
  color: #ffffff;
}

.header-nav {
  display: flex;
  gap: 40rpx;
}

.nav-item {
  font-size: 16px;
  color: #ffffff;
  position: relative;
}

.nav-item:after {
  content: "";
  position: absolute;
  bottom: -5rpx;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #6c63ff;
  transition: width 0.3s ease;
}

.nav-item:hover:after {
  width: 100%;
}

.mobile-menu-btn {
  display: none;
}

/* Hero Section Styles */
.hero-section {
  height: 100vh;
  min-height: 1000rpx;
  background: linear-gradient(135deg, #351968 0%, #1a1a35 100%);
  position: relative;
  overflow: hidden;
  padding-top: 100rpx;
}

.hero-content {
  display: flex;
  height: 100%;
  padding: 0 60rpx;
}

.hero-left {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  z-index: 2;
}

.company-name {
  font-size: 80px;
  font-weight: 800;
  color: #ffffff;
  margin-bottom: 20rpx;
  letter-spacing: -1px;
}

.slogan {
  font-size: 32px;
  font-weight: 300;
  color: #6c63ff;
  margin-bottom: 40rpx;
}

.hero-description {
  margin-bottom: 60rpx;
  max-width: 600rpx;
}

.hero-description text {
  font-size: 18px;
  line-height: 1.6;
  color: rgba(255, 255, 255, 0.8);
}

.cta-container {
  display: flex;
  gap: 30rpx;
}

.primary-btn {
  background-color: #6c63ff;
  color: white;
  padding: 20rpx 60rpx;
  border-radius: 50rpx;
  font-size: 18px;
  font-weight: 600;
  border: none;
  transition: all 0.3s ease;
}

.primary-btn:hover {
  background-color: #5a52d5;
  transform: translateY(-5rpx);
}

.secondary-btn {
  background-color: transparent;
  color: white;
  padding: 20rpx 60rpx;
  border-radius: 50rpx;
  font-size: 18px;
  font-weight: 600;
  border: 2px solid #6c63ff;
  transition: all 0.3s ease;
}

.secondary-btn:hover {
  background-color: rgba(108, 99, 255, 0.1);
}

.hero-right {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
}

.hero-image {
  width: 600rpx;
  height: 600rpx;
  border-radius: 20rpx;
  box-shadow: 0 20rpx 50rpx rgba(0, 0, 0, 0.3);
  transform: perspective(1000px) rotateY(-10deg);
  transition: all 0.5s ease;
}

.hero-image:hover {
  transform: perspective(1000px) rotateY(0deg);
}

.floating-elements {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}

.float-element {
  position: absolute;
  border-radius: 50%;
  opacity: 0.2;
  background: linear-gradient(135deg, #6c63ff 0%, #ff6cab 100%);
}

.float-1 {
  width: 300rpx;
  height: 300rpx;
  top: 10%;
  left: 10%;
  animation: float 15s ease-in-out infinite;
}

.float-2 {
  width: 200rpx;
  height: 200rpx;
  top: 60%;
  right: 15%;
  animation: float 12s ease-in-out infinite 2s;
}

.float-3 {
  width: 150rpx;
  height: 150rpx;
  bottom: 20%;
  left: 30%;
  animation: float 10s ease-in-out infinite 1s;
}

@keyframes float {
  0% {
    transform: translate(0, 0);
  }
  50% {
    transform: translate(30rpx, 30rpx);
  }
  100% {
    transform: translate(0, 0);
  }
}

/* Section Title Styles */
.section-title-container {
  text-align: center;
  margin: 100rpx 0 60rpx;
}

.section-title {
  font-size: 48px;
  font-weight: 700;
  color: #351968;
  margin-bottom: 20rpx;
  position: relative;
  display: inline-block;
}

.section-title:after {
  content: "";
  position: absolute;
  bottom: -10rpx;
  left: 50%;
  transform: translateX(-50%);
  width: 100rpx;
  height: 4px;
  background-color: #6c63ff;
}

.section-subtitle {
  font-size: 18px;
  color: #666666;
  max-width: 600rpx;
  margin: 0 auto;
}

/* Services Section Styles */
.services-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 40rpx;
  padding: 0 40rpx;
  margin-bottom: 100rpx;
}

.service-tile {
  width: 300rpx;
  height: 400rpx;
  background-color: white;
  border-radius: 20rpx;
  box-shadow: 0 10rpx 30rpx rgba(0, 0, 0, 0.1);
  padding: 40rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.service-tile:hover {
  transform: translateY(-20rpx);
  box-shadow: 0 20rpx 40rpx rgba(0, 0, 0, 0.15);
}

.service-tile:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 6px;
  background: linear-gradient(90deg, #6c63ff 0%, #ff6cab 100%);
}

.service-icon-container {
  width: 120rpx;
  height: 120rpx;
  margin-bottom: 30rpx;
}

.service-icon {
  width: 100%;
  height: 100%;
}

.service-name {
  font-size: 20px;
  font-weight: 600;
  color: #351968;
  margin-bottom: 20rpx;
}

.service-description {
  font-size: 14px;
  color: #666666;
  flex-grow: 1;
}

/* Creative Storytelling Section Styles */
.storytelling-section {
  padding: 80rpx 40rpx;
  background-color: #f9f9ff;
  position: relative;
  overflow: hidden;
}

.timeline-container {
  position: relative;
  padding: 60rpx 0;
  margin: 0 auto;
  max-width: 700rpx;
}

.timeline-line {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 50%;
  width: 4px;
  background-color: #6c63ff;
  transform: translateX(-50%);
}

.timeline-steps {
  position: relative;
}

.timeline-step {
  display: flex;
  margin-bottom: 80rpx;
  position: relative;
}

.timeline-step:nth-child(odd) {
  justify-content: flex-start;
}

.timeline-step:nth-child(even) {
  justify-content: flex-end;
}

.timeline-dot {
  position: absolute;
  top: 20rpx;
  left: 50%;
  width: 30rpx;
  height: 30rpx;
  background-color: #6c63ff;
  border-radius: 50%;
  transform: translateX(-50%);
  z-index: 2;
}

.timeline-content {
  width: 300rpx;
  background-color: white;
  padding: 30rpx;
  border-radius: 10rpx;
  box-shadow: 0 5rpx 15rpx rgba(0, 0, 0, 0.1);
  position: relative;
}

.timeline-step:nth-child(odd) .timeline-content {
  margin-right: 80rpx;
}

.timeline-step:nth-child(even) .timeline-content {
  margin-left: 80rpx;
}

.timeline-step-number {
  position: absolute;
  top: -20rpx;
  left: 20rpx;
  width: 40rpx;
  height: 40rpx;
  background-color: #ff6cab;
  color: white;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bold;
  font-size: 16px;
}

.timeline-title {
  font-size: 18px;
  font-weight: 600;
  color: #351968;
  margin-bottom: 10rpx;
  margin-top: 20rpx;
}

.timeline-description {
  font-size: 14px;
  color: #666666;
}

.african-patterns {
  margin-top: 80rpx;
  width: 100%;
  overflow: hidden;
}

.pattern-image {
  width: 100%;
  height: 200rpx;
}

/* Portfolio Section Styles */
.portfolio-section {
  padding: 80rpx 0;
}

.portfolio-scroll {
  width: 750rpx;
  overflow: auto;
}

.portfolio-container {
  display: flex;
  padding: 20rpx 40rpx;
  gap: 30rpx;
}

.portfolio-item {
  flex-shrink: 0;
  width: 500rpx;
  height: 350rpx;
  border-radius: 20rpx;
  overflow: hidden;
  position: relative;
  box-shadow: 0 10rpx 30rpx rgba(0, 0, 0, 0.15);
  transition: all 0.3s ease;
}

.portfolio-item:hover {
  transform: scale(1.05);
}

.portfolio-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.portfolio-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 30rpx;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
  color: white;
}

.portfolio-title {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 10rpx;
}

.portfolio-category {
  font-size: 14px;
  opacity: 0.8;
}

/* Location Section Styles */
.location-section {
  padding: 80rpx 40rpx;
  background-color: #f9f9ff;
}

.location-container {
  display: flex;
  gap: 60rpx;
  margin-top: 60rpx;
}

.map-container {
  flex: 1;
  border-radius: 20rpx;
  overflow: hidden;
  box-shadow: 0 10rpx 30rpx rgba(0, 0, 0, 0.1);
}

.map-image {
  width: 100%;
  height: 400rpx;
  object-fit: cover;
}

.location-info {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.info-item {
  display: flex;
  align-items: center;
  margin-bottom: 30rpx;
}

.info-icon {
  margin-right: 20rpx;
  width: 24px;
  height: 24px;
  flex-shrink: 0;
}

.info-text {
  font-size: 16px;
  color: #333333;
}

.social-links {
  display: flex;
  gap: 30rpx;
  margin-top: 40rpx;
}

.social-icon {
  width: 50rpx;
  height: 50rpx;
  border-radius: 50%;
  background-color: #f0f0f0;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.3s ease;
}

.social-icon:hover {
  background-color: #6c63ff;
}

.social-icon:hover uni-icons {
  color: white;
}

/* Newsletter Section Styles */
.newsletter-section {
  padding: 80rpx 40rpx;
  background-color: #351968;
}

.newsletter-container {
  max-width: 700rpx;
  margin: 0 auto;
  text-align: center;
}

.newsletter-title {
  font-size: 36px;
  font-weight: 700;
  color: white;
  margin-bottom: 20rpx;
}

.newsletter-description {
  font-size: 16px;
  color: rgba(255, 255, 255, 0.8);
  margin-bottom: 40rpx;
}

.newsletter-form {
  display: flex;
  max-width: 600rpx;
  margin: 0 auto;
}

.newsletter-input {
  flex: 1;
  height: 80rpx;
  padding: 0 30rpx;
  border: none;
  border-radius: 40rpx 0 0 40rpx;
  font-size: 16px;
}

.newsletter-button {
  height: 80rpx;
  padding: 0 40rpx;
  background-color: #6c63ff;
  color: white;
  border: none;
  border-radius: 0 40rpx 40rpx 0;
  font-size: 16px;
  font-weight: 600;
}

/* Footer Styles */
.footer {
  background-color: #1a1a35;
  color: white;
  padding: 80rpx 40rpx 0;
  position: relative;
}

.footer-top {
  display: flex;
  justify-content: space-between;
  margin-bottom: 80rpx;
}

.footer-logo {
  max-width: 300rpx;
}

.footer-company-name {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 10rpx;
  display: block;
}

.footer-slogan {
  font-size: 16px;
  color: #6c63ff;
  display: block;
}

.footer-links {
  display: flex;
  gap: 80rpx;
}

.footer-column {
  display: flex;
  flex-direction: column;
}

.footer-column-title {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 30rpx;
  color: white;
}

.footer-link {
  font-size: 14px;
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 20rpx;
  transition: color 0.3s ease;
}

.footer-link:hover {
  color: #6c63ff;
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40rpx 0;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.copyright {
  font-size: 14px;
  color: rgba(255, 255, 255, 0.5);
}

.footer-bottom-links {
  display: flex;
  gap: 30rpx;
}

.policy-link {
  font-size: 14px;
  color: rgba(255, 255, 255, 0.5);
  transition: color 0.3s ease;
}

.policy-link:hover {
  color: white;
}

.cityscape-container {
  width: 100%;
  height: 200rpx;
  overflow: hidden;
  margin-top: 40rpx;
}

.cityscape-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Media Queries for Responsive Design */
@media screen and (max-width: 768px) {
  .hero-content {
    flex-direction: column;
  }

  .hero-left,
  .hero-right {
    width: 100%;
  }

  .hero-image {
    margin-top: 60rpx;
  }

  .header-nav {
    display: none;
  }

  .mobile-menu-btn {
    display: block;
  }

  .footer-top {
    flex-direction: column;
    gap: 60rpx;
  }

  .footer-links {
    flex-wrap: wrap;
    gap: 40rpx;
  }

  .location-container {
    flex-direction: column;
  }
}
</style>
