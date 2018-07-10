<template>
  <div class="resume mt-3 py-4">
    <div class="row">
      <div class="col-1">
        <img class="rounded-circle img-fluid" src="https://github.com/tobiasdalhof.png" alt="Tobias Dalhof">
      </div>
      <div class="col d-flex justify-content-center flex-column">
        <div>
          <h1 class="mt-0 mb-2">{{ getGreeting() }}. Ich bin Tobias Dalhof und das ist mein Résumé.</h1>
          <p class="m-0"><a href="https://github.com/tobiasdalhof" target="_blank"><i class="fab fa-github mr-2"></i>Github</a> - <a href="https://www.xing.com/profile/Tobias_Dalhof" target="_blank"><i class="fab fa-xing mr-2"></i>Xing</a> - <a href="https://www.linkedin.com/in/tobias-dalhof/" target="_blank"><i class="fab fa-linkedin mr-2"></i>LinkedIn</a> | *20.10.1993 - aus <a href="https://www.google.de/maps/search/Ellwangen/@48.9649778,10.1094564,12z" target="_blank">Ellwangen</a></p>
        </div>
      </div>
    </div>
    <div class="mt-3">
      <h2>Berufserfahrung</h2>
      <div class="work-experience">
        <div class="row mb-5">
          <div class="col-12 col-sm-4">
            <div class="time mb-4 mb-sm-0">
              <div class="mb-2 font-weight-bold">07/2017 - heute</div>
              <div>Webentwickler @ <a href="https://goo.gl/Ss8X7M" target="_blank">Alfa GmbH</a></div>
            </div>
          </div>
          <div class="col">
            <div class="description">
              <div class="mb-2 font-weight-bold">Aufgabenbereiche</div>
              <ul class="pl-3 mb-3">
                <li>Weiterentwicklung der Magento Shops (Extensions und Templates)</li>
                <li>Landingpages und Produktseiten erstellen</li>
                <li>OnPage Optimierung</li>
                <li>Conversion Optimierung</li>
                <li>Web Analytics</li>
              </ul>
              <div class="mb-2 font-weight-bold">Projektbeispiele</div>
              <ul class="pl-3 mb-0">
                <li><a href="https://goo.gl/v7RjSs" target="_blank">Handwerker wirbt Handwerker</a></li>
                <li><a href="https://goo.gl/PVN2qZ" target="_blank">Alfa Plus</a></li>
                <li><a href="https://goo.gl/ib2fLq" target="_blank">Alfa App (WebView)</a></li>
                <li><a href="https://goo.gl/QB5ucj" target="_blank">ETAG Verbrauchsrechner</a></li>
              </ul>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-4">
            <div class="time mb-4 mb-sm-0">
              <div class="mb-2 font-weight-bold">09/2014 - 07/2017</div>
              <div class="mb-1">Ausbildung Informatikkaufmann @ <a href="https://goo.gl/Ss8X7M" target="_blank">Alfa GmbH</a></div>
              <div>Unterrichtet @ <a target="_blank" href="https://www.ks-heidenheim.de/">Kaufmännische Schule Heidenheim</a></div>
            </div>
          </div>
          <div class="col">
            <div class="description">
              <div class="font-weight-bold mb-3">
                <div class="row">
                  <div class="col-6">IHK Abschlussprüfung</div>
                  <div class="col">85/100</div>
                </div>
              </div>
              <div class="font-weight-bold mb-2">Prüfung Teil A</div>
              <div class="mb-1">
                <div class="row">
                  <div class="col-6">Betriebliche Projektarbeit</div>
                  <div class="col">98/100</div>
                </div>
              </div>
              <div class="mb-3">
                <div class="row">
                  <div class="col-6">Präsentation & Fachgespräch</div>
                  <div class="col">90/100</div>
                </div>
              </div>
              <div class="mb-2">Projektthema: "Amazon Versandbestätigungen automatisieren - Webanwendung für den automatischen Versand von Versandbestätigungen für Amazon-Bestellungen"</div>
              <div class="mb-4"><a target="_blank" href="/ihk-betriebliche-projektarbeit-doku.pdf"><i class="far fa-file-pdf mr-2"></i>Projektdokumentation</a></div>

              <div class="font-weight-bold mb-2">Prüfung Teil B</div>
              <div class="mb-2">
                <div class="row">
                  <div class="col-6">Ganzheitliche Aufgabe I</div>
                  <div class="col">76/100</div>
                </div>
              </div>
              <div class="mb-2">
                <div class="row">
                  <div class="col-6">Ganzheitliche Aufgabe II</div>
                  <div class="col">76/100</div>
                </div>
              </div>
              <div class="mb-4">
                <div class="row">
                  <div class="col-6">Wirtschafts- und Sozialkunde</div>
                  <div class="col">72/100</div>
                </div>
              </div>
              <div>
                <div class="row">
                  <div class="col-6">
                    <div class="font-weight-bold mb-2">KMK-Fremdsprachen-Zertifikat</div>
                    <div>Englisch, Niveaustufe II (B1)</div>
                  </div>
                  <div class="col font-weight-bold">118/130 (90,8 %)</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="">
      <h2>Skills</h2>
      <div v-for="category in skillCategories" :key="category.title" class="mb-4">
        <h3 class="skill-title mb-3 mt-0"><span>{{ category.title }}</span></h3>
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

    <div class="">
      <h2>Side Projects</h2>
      <div>
        <ul> 
          <li><a href="https://softwarekompass.de" target="_blank">Softwarekompass.de</a> - Affiliate Projekt; Datenbank mit Business-Software</li>
        </ul>
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
            '<i class="fas fa-database"></i> Relationale Datenbanken',
          ],
        },
        {
          title: 'Frontend',
          labelColor: '#1565C0',
          skills: [
            '<i class="fab fa-html5"></i> HTML5',
            '<i class="fab fa-css3"></i> CSS3',
            '<i class="fab fa-sass"></i> Scss',
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
            '<i class="fas fa-code"></i> Visual Studio Code',
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
            'Node.js',
            'Golang',
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
}
.work-experience {
  font-size: .8em;
  .time {
    color: #EEEEEE;
  }
  .description {
    color: #F5F5F5;
  }
}
.skill-title {
  position: relative;
  font-size: .8em;
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
