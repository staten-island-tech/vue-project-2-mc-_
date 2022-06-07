<template>
  <div class="Dark">
    <h1 class="Header">Armed Detective Agency</h1>
    <nav class="NavBar">
      <a class="navbar-item" href="#Description">Description</a>
      <a class="navbar-item" href="#Admission">Admission Process</a>
      <a class="navbar-item" href="#Cases">Cases</a>
      <a class="navbar-item" href="#Staff">Meet the Staff</a>
    </nav>
    <NuxtLink class="BTN" to="/light">Change Theme</NuxtLink>
    <img class="Agency" :src="Agency" alt="Agency Building" />
    <h2 class="Section-Heading" id="Description">Description</h2>
    <h3 class="Section">
      The Armed Detective Agency is an organization that focuses on solving
      crimes that are considered to be far too violent or difficult for the
      metropolitan police to handle. The crimes that we handle often involve the
      supernatural, which is why nearly all detectives have abilities. The
      agency has been issued a skilled business permit by the Special Division
      for Unusual Powers, which permits our activities as a skill-user
      organization and allows the agency to legally operate. All official agency
      members are affected by the current president, Yukichi Fukuzawa's ability,
      All Men are Equal. All Men are Equal is an inhibition ability that allows
      Fukuzawa to suppress the abilities of his subordinates, essentially
      allowing the agency members with uncontrollable abilities to partially
      control their abilities. Applicants must pass their entrance exams in
      order to be included within the range of this ability. Please note that
      the agency's licensed staff had been granted police-like authority, which
      grants us the right to carry guns and knives under certain conditions.
    </h3>
    <h2 class="Section-Heading" id="Admission">Admission Process</h2>
    <h3 class="Section">
      In order for someone to officially join the agency, they must first take
      an entrance exam that assesses whether or not they possess the right
      qualities needed for an agency member. There is no set entrance exam and
      the exam that the candidates take generally depends on the current
      situation the agency and/or candidate are in. Possible exams may be, but
      are not limited to: handling a case or solving an in-house issue. The exam
      generally evaluates the candidate's righteousness,prowess, wisdom,
      morality, emotions, willingness to risk their lives to save others as well
      as their genuineness of spirit. The test supervisor will then watch and
      examine the candidate's actions in order to determine whether or not they
      will be a good fit to the detective agency.
    </h3>
    <h2 class="Section-Heading" id="Cases">List of Cases Handled</h2>
    <div class="Section">
      <h3>Serial Disappearances of Yokohama Visitors Case</h3>
      <h3>Azure Apostle Abandoned Building Case</h3>
      <h3>Azure Apostle Bomb Threat Case</h3>
      <h3>Kyushu Murder Case</h3>
      <h3>Azure Apostle Aircraft Attack Case</h3>
      <h3>Man-Eating Tiger Case</h3>
      <h3>Hokuriku Massacre Case</h3>
      <h3>Yamagiwa Murder Case</h3>
      <h3>Car Explosion Case</h3>
      <h3>The Incineration of Yokohama</h3>
      <h3>Orphanage Director Accident Case</h3>
      <h3>Kindaichi Murder Case</h3>
      <h3>Decay of the Angel Case</h3>
      <h3>Serial Skill User Suicide Phenomenon</h3>
    </div>
    <h2 class="Section-Heading" id="Staff">Meet the Staff</h2>
    <h2 class="Section-Heading">Founder</h2>
    <Card
      v-for="Founder in Founders"
      :key="Founder.Name"
      :Name="Founder.Name"
      :Ability="Founder.Ability"
      :Image="Founder.Image"
    ></Card>
    <h2 class="Section-Heading">Detectives</h2>
    <Card
      v-for="Member in Members"
      :key="Member.Name"
      :Name="Member.Name"
      :Ability="Member.Ability"
      :Image="Member.Image"
    ></Card>
    <h2 class="Section-Heading">Contact Info</h2>
    <div class="Footer">
      <h3>Phone: XXX-XXX-XXXX</h3>
      <h3>Twitter: @busou_da_jp</h3>
    </div>
  </div>
</template>

<script>
import Card from '../components/Card.vue'
import { gsap } from 'gsap'

export default {
  name: 'ADA',
  components: { Card },
  data() {
    return {
      Agency:
        'https://i.pinimg.com/736x/87/98/84/8798849c790aaceebd6ed4b8f3d183fb.jpg',
      Founders: [
        {
          Name: 'Yukichi Fukuzawa',
          Ability: 'All Men are Equal',
          Image:
            'https://i.pinimg.com/originals/7f/17/d2/7f17d28ebd32e4c478195a1654cbeaf1.jpg',
        },
      ],
      Members: [
        {
          Name: 'Doppo Kunikida',
          Ability: 'The Matchless Poet',
          Image:
            'https://i.pinimg.com/736x/16/ee/53/16ee531153f0313a3074025be6736422.jpg',
          Des: '',
        },
        {
          Name: 'Ranpo Edogawa',
          Ability: 'Super Deduction',
          Image:
            'https://i.pinimg.com/736x/fb/a6/3e/fba63e8f50a6e6c6f2cf56001d6be3cc.jpg',
          Des: '',
        },
        {
          Name: 'Akiko Yosano',
          Ability: 'Thou Shall Not Die',
          Image:
            'https://i.pinimg.com/736x/8d/ef/fe/8deffe48cffdb3295ead113ab01c0852.jpg',
          Des: '',
        },
        {
          Name: 'Osamu Dazai',
          Ability: 'No Longer Human',
          Image:
            'https://i.pinimg.com/736x/40/3e/50/403e509fe0d8e8f127cf144746e0d97f.jpg',
          Des: '',
        },
        {
          Name: 'Jun’ichiro Tanizaki',
          Ability: 'Light Snow',
          Image:
            'https://i.pinimg.com/236x/5f/a6/b0/5fa6b0cbce7e45500352acf648dfbf4c.jpg?nii=t',
          Des: '',
        },
        {
          Name: 'Kenji Miyazawa',
          Ability: 'Undefeated by the Rain',
          Image:
            'https://i.pinimg.com/originals/3e/c0/9e/3ec09ebc50542b9d3bd7d88f79ca268a.jpg',
          Des: '',
        },
        {
          Name: 'Atsushi Nakajima',
          Ability: 'Beast Beneath the Moonlight',
          Image:
            'https://i.pinimg.com/474x/34/33/e7/3433e7fb4dfbce6169bee580502040dd.jpg',
          Des: '',
        },
        {
          Name: 'Kyoka Izumi',
          Ability: 'Demon Snow',
          Image:
            'https://i.pinimg.com/736x/76/d0/e4/76d0e4d6839bd3f1ab24fac6b5787cb3.jpg',
          Des: '',
        },
      ],
    }
  },
  mounted: function () {
    gsap.from('.Agency', {
      duration: 5,
      opacity: 0,
    })
    gsap.from('.navbar-item', {
      duration: 2,
      scale: 0.5,
      opacity: 0.5,
      ease: 'slow(0.7, 0.7, false)',
    })
    gsap.from('.Header', {
      duration: 2,
      scale: 0.5,
      opacity: 0.5,
      ease: 'expo.inOut',
    })
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Quintessential&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap');

html,
body,
* {
  margin: 0%;
  padding: 0%;
  font-size: 42px;
  text-align: center;
  align-items: center;
  background-color: var(--Background);
  font-family: 'Dancing Script', cursive;
}
h1,
h2,
h3 {
  color: var(--Text);
}
:root {
  --Blue: #66779f;
  --Gray: #dee0e2;
  --White: #ffffff;
  --Black: #000000;
  --DarkBlue: #030562;
}
.Dark {
  --Text: var(--White);
  --Secondary: var(--DarkBlue);
  --Background: var(--Black);
}
.Light {
  --Text: var(--Black);
  --Secondary: var(--Blue);
  --Background: var(--Gray);
}
.navbar-item {
  font-size: 0.8rem;
  color: var(--Text);
  margin-right: 1.5rem;
  text-decoration: underline;
  font-family: 'Quintessential', cursive;
}
.navbar-item:hover {
  color: var(--Secondary);
  text-decoration-color: var(--Secondary);
}
.NavBar {
  text-align: center;
  white-space: nowrap;
}
.BTN {
  padding: 5px;
  font-size: 0.5rem;
  color: var(--Text);
  border-width: 2px;
  margin-bottom: 0.1rem;
  border-color: var(--Text);
  text-decoration: underline;
  font-family: 'Quintessential', cursive;
}
.BTN:hover {
  color: var(--Secondary);
  border-color: var(--Secondary);
  text-decoration-color: var(--Secondary);
}
.Agency {
  width: 100%;
}
.Footer {
  margin-top: 0.5%;
}
.Header {
  font-size: 1.6rem;
  text-decoration: underline;
  font-family: 'Quintessential', cursive;
}
.Section {
  margin-left: 5%;
  margin-right: 5%;
  margin-bottom: 0.5%;
}
.Section-Heading {
  font-size: 1rem;
  text-decoration: underline;
  background-color: var(--Secondary);
  font-family: 'Quintessential', cursive;
}
.Section-Heading:hover {
  color: var(--Background);
}
@media all and (max-width: 900px) {
  html,
  body,
  * {
    font-size: 25px;
  }
  .navbar-item {
    font-size: 25px;
  }
  .NavBar {
    white-space: normal;
  }
  .BTN {
    font-size: 1rem;
  }
  .Header {
    font-size: 2rem;
  }
  .Section-Heading {
    font-size: 1rem;
  }
}
</style>