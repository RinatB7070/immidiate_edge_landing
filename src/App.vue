<template>
  <AppHeader
    :isMob="this.isMob"
    :isTabl="this.isTabl"
  ></AppHeader>
  <AppOffer
    :logos="this.logos"
  ></AppOffer>
  <RunningLine
    :people="this.rlPeople"
  ></RunningLine>
  <RichPeople></RichPeople>
  <BitCostsHeader></BitCostsHeader>
  <BitCosts></BitCosts>
  <CTA></CTA>
  <PeopleForm
    :formPeople="this.formPeople1"
    :isTabl="this.isTabl"
  ></PeopleForm>
  <AppAdvantages></AppAdvantages>
  <RunningLine
    :people="this.rlPeople"
  ></RunningLine>
  <AnotherAdd></AnotherAdd>
  <PeopleForm
    :formPeople="this.formPeople2"
    :isTabl="this.isTabl"
  ></PeopleForm>
  <FacebookCom></FacebookCom>
  <FooterForm
    :logos="this.logos"
  ></FooterForm>
  <AppFooter></AppFooter>
  <teleport to="body">
    <PeoplePopup
      :justMadePeople="this.justMadePeople"
    ></PeoplePopup>
  </teleport>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppOffer from './components/AppOffer.vue'
import RunningLine from './components/RunningLine.vue'
import RichPeople from './components/RichPeople.vue'
import BitCostsHeader from './components/BitCostsHeader.vue'
import BitCosts from './components/BitCosts.vue'
import CTA from './components/CTA.vue'
import PeopleForm from './components/PeopleForm.vue'
import AppAdvantages from './components/AppAdvantages.vue'
import AnotherAdd from './components/AnotherAdd.vue'
import FacebookCom from './components/FacebookCom.vue'
import FooterForm from './components/FooterForm.vue'
import AppFooter from './components/AppFooter.vue'
import PeoplePopup from './components/PeoplePopup.vue'

export default {
  data () {
    const mediaMob = window.matchMedia('(max-width: 640px)');
    const mediaTabl = window.matchMedia('(max-width: 800px)');
    return {
      mediaMob,
        mediaTabl,
        isMob: mediaMob.matches,
        isTabl: mediaTabl.matches,
        logos: ['symantec', 'mcafee', 'verisign', 'ssl', 'geotrust'],
        rlPeople: [
        {
          img: '1',
          name: 'D Ward',
          profit: 547
        },
        {
          img: '2',
          name: 'I Cox',
          profit: 483
        },
        {
          img: '3',
          name: 'J Payne',
          profit: 566
        },
        {
          img: '4',
          name: 'B Sims',
          profit: 289
        },
        {
          img: '5',
          name: 'l Edwards',
          profit: 789
        },
        {
          img: '6',
          name: 'W Woods',
          profit: 279
        },
        {
          img: '7',
          name: 'B Medina',
          profit: 324
        },
        {
          img: '8',
          name: 'B Medina',
          profit: 443
        },
        {
          img: '9',
          name: 'C Perkins',
          profit: 820
        },
        {
          img: '10',
          name: 'G Baker',
          profit: 761
        },
        ],
        formPeople1: [
          {
            img: '1',
            name: 'Jonathan Mulberry',
            quote: 'I just want to say a great big Thank you because Immediate Edge has really turned my life around. In a matter of weeks, I’ve been able to quit my job!',
            amount: '$ 5,977'
          },
          {
            img: '2',
            name: 'Delilah Adams',
            quote: 'Man, this thing actually works! It’s amazing really. I’ve only used it for a couple of weeks and I’ve already made more money from it than I do busting my butt off at work for months!',
            amount: '$ 11,369'
          },
          {
            img: '3',
            name: 'Simon Horsham',
            quote: 'I received my notice two weeks ago. With no alternatives I thought my life would be over. Now Im making about $13,261.42 every week! And for the first time in 2 months Im not in the dark. Thanks Edwin!',
            amount: '$ 33,426'
          }
        ],
        formPeople2: [
          {
            img: '4',
            name: 'Lewis Tucker',
            quote: 'I can’t get over it. Like $43,568 in just 30 days. I am so grateful.',
            amount: '$ 12,896'
          },
          {
            img: '5',
            name: 'Georgina Barry',
            quote: 'My trading account now has $231,952 in it. Can you believe it!',
            amount: '$ 49,279'
          },
          {
            img: '6',
            name: 'Owen Spencer',
            quote: 'I am so speechless. I’ve never seen numbers like this before. Thank You Immediate Edge',
            amount: '$ 7,899'
          }
        ],
        justMadePeople: [
          {
            img: '1',
            name: 'M Hunter',
            profit: 539
          },
          {
            img: '2',
            name: 'Z Shelton',
            profit: 955
          },
          {
            img: '3',
            name: 'J Gutierrez',
            profit: 424
          },
          {
            img: '4',
            name: 'P Morgan',
            profit: 202
          },
          {
            img: '5',
            name: 'R Harrison',
            profit: 251
          },
          {
            img: '6',
            name: 'E Mitchel',
            profit: 784
          },
          {
            img: '7',
            name: 'W Bates',
            profit: 278
          },
          {
            img: '8',
            name: 'R Stephens',
            profit: 681
          },
        ]
    }
  },
  mounted() {
    this.mediaMob.addEventListener('change', () => {
      this.isMob = this.mediaMob.matches;
    }) 
    this.mediaTabl.addEventListener('change', () => {
      this.isTabl = this.mediaTabl.matches;
    }) 
  },
  components: {
    AppHeader,
    AppOffer,
    RunningLine,
    RichPeople,
    BitCostsHeader,
    BitCosts,
    CTA,
    PeopleForm,
    AppAdvantages,
    AnotherAdd,
    FacebookCom,
    FooterForm,
    AppFooter,
    PeoplePopup
  }
}
</script>