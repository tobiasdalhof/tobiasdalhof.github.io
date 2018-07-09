<template>
  <div class="cv">
    <div class="container">
      <h1>{{ getGreeting() }}. Ich bin Tobias Dalhof und das ist mein Curriculum Vitae.</h1>
      <div>
        <h2>Berufserfahrung</h2>
        <div v-for="work in workExperience" :key="work.timeSpan" class="work-experience">
          <div class="time">
            <div>
              {{ work.timeSpan }}
            </div>
          </div>
          <div class="description">
            <div>
              {{ work.title }}
            </div>
          </div>
        </div>
      </div>
      <div>
        <h2>Skills</h2>
        <div v-for="category in skillCategories" :key="category.title">
          <h3 class="skill-title"><span>{{ category.title }}</span></h3>
          <div class="skills">
            <span 
              v-for="skill in category.skills" 
              :key="skill"
              class="label"
              :style="`background-color: ${category.labelColor}`">
              <span v-html="skill"></span>
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'resume',
  data () {
    return {
      skillCategories: [
        {
          title: 'Backend',
          labelColor: '#283593',
          skills: [
            '<i class="fab fa-php"></i> PHP 7',
            '<i class="fab fa-laravel"></i> Laravel 5.6',
            '<i class="fab fa-magento"></i> Magento 1.7 - 1.9',
            '<i class="fas fa-database"></i> SQL',
          ],
        },
        {
          title: 'Frontend',
          labelColor: '#1565C0',
          skills: [
            '<i class="fab fa-html5"></i> HTML5',
            '<i class="fab fa-css3"></i> CSS3',
            '<i class="fab fa-sass"></i> Sass',
            '<i class="fab fa-js"></i> JavaScript',
            '<i class="fas fa-mobile-alt"></i> <i class="fas fa-desktop"></i> Responsive Design',
            '<i class="fab fa-vuejs"></i> Vue.js',
            '<i class="fas fa-toolbox"></i> Vuetify',
            '<i class="fas fa-toolbox"></i> Bootstrap 3 & 4',
            '<i class="fas fa-toolbox"></i> jQuery',
            '<i class="far fa-envelope"></i> MJML Mail Templates',
          ],
        },
        {
          title: 'Tools',
          labelColor: '#00838F',
          skills: [
            '<i class="fab fa-git"></i> Git',
            '<i class="fab fa-docker"></i> Docker',
            '<i class="fab fa-npm"></i> NPM',
            '<i class="fas fa-wrench"></i> Composer',
            '<i class="fas fa-wrench"></i> Webpack',
            '<i class="fas fa-code"></i> VSCode',
          ],
        },
        {
          title: 'Sonstiges',
          labelColor: '#00695C',
          skills: [
            '<i class="fas fa-cart-plus"></i> B2B & B2C E-Commerce Erfahrung',
            '<i class="fas fa-bullseye"></i> Landingpages',
            '<i class="far fa-chart-bar"></i> Google Analytics',
            '<i class="far fa-chart-bar"></i> Matomo (PIWIK)',
            '<i class="fas fa-tachometer-alt"></i> OnPage Optimierung',
            '<i class="fas fa-tachometer-alt"></i> Seobility',
            '<i class="fas fa-chart-line"></i> Conversion Optimierung',
            '<i class="fas fa-flask"></i> A/B Testing',
            '<i class="fas fa-flask"></i> Google Optimize',
            '<i class="fas fa-flask"></i> Optimizely',
            '<i class="far fa-image"></i> Adobe Photoshop CC',
          ],
        },
        {
          title: 'Erste Erfahrungen mit ...',
          labelColor: '#424242',
          skills: [
            'Unit Tests',
            'TDD',
            'Golang',
            'Node.js',
            'Redis',
            'Microservices',
            'DigitalOcean',
            'Amazon S3',
            'Amazon Cloudfront CDN',
            'Amazon RDS',
            'Google Cloud Compute Engine',
            'Google Cloud Kubernetes Engine',
            'Google Cloud SQL',
            'Google Cloud Datastore (NoSQL)',
            'Amazon Marketplace Web Service',
            'Shopify REST Admin API',
            'Google Ads',
            'Facebook Ads',
            'Amazon Seller Central PPC Ads',
            '...',
          ],
        },
      ],
      greetings: [
        'Hi', 'Hey', 'Moin',
      ],
    }
  },
  methods: {
    getGreeting () {
      return this.greetings[Math.floor(Math.random()*this.greetings.length)]
    }
  }
}
</script>

<style lang="scss">
  .container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 0 15px;
  }
  h1 {
    font-size: 1.8em;
    color: #FAFAFA;
  }
  h2 {
    margin: 25px 0;
    font-size: 1.2em;
  }
  .label {
    display: inline-block;
    padding: 8px 10px;
    border-radius: 999px;
    color: #E0E0E0;
    font-size: .8em;
    font-weight: 400;
    cursor: default;
    user-select: none;
    white-space: nowrap;
    &:hover {
      color: #FAFAFA;
    }
  }
  .work-experience {
    display: flex;
    margin-bottom: 15px;
    .time {
      width: 250px;
      color: #F5F5F5;
    }
    .description {
      flex: 1;
    }
  }
  .skill-title {
    margin-bottom: 20px;
    position: relative;
    font-size: .9em;
    font-weight: 400;
    color: #757575;
    span {
      display: inline-block;
      padding-right: 10px;
      background-color: #212121;
    }
    &:after {
      content: ' ';
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 0.5em;
      border-top: 1px dotted #444;
      z-index: -1;
    }
  }
  .skills {
    margin-bottom: 20px;
    .label {
      margin-right: 8px;
      margin-bottom: 10px;
      &:last-child {
        margin-right: 0;
      }
    }
  }
</style>
