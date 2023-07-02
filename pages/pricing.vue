<template>
<v-container>
 <v-col align="center">
    <PricingSelector />
    <div class="cards-grid">
      <PricingVariant v-bind:data="data[type][0]"/>
      <PricingVariant v-bind:data="data[type][1]" />
      <PricingVariant v-bind:data="data[type][2]"/>
    </div>
  
  </v-col>
</v-container>
</template>

<script>
export default {
  data () {
  return {
    type: 0,
    data: [
      [
      { title: 'Starter',
      price: 'Free',
      color: 'grey',
      time: 'Forever',
      features: [
        '3 Figma and 3 FigJam files',
        'Unlimited personal files',
        'Unlimited collaborators',
        'Plugins and templates',
        'Mobile app',
        'Music player',
        'Ready-made templates',
      ]
      },
      { title: 'FigJam Professional',
      price: '$3  per editor/month',
      color: 'orange',
      time: 'Forever',
      features: [
        'Unlimited FigJam files',
        'Open sessions',
        'Sharing permissions',
        'Team libraries',
        'Audio conversations',
        'Voting',
      ]
      },
      { title: 'FigJam Organization',
      price: '$5  per editor/month',
      color: 'violet',
      time: 'Forever',
      features: [
        'Org-wide libraries',
        'Centralized content management',
        'Custom templates',
        'Custom color palettes',
        'Unified admin and billing',
        'Private plugins and widgets',
        'Single sign-on',
      ]
      },
    ],
    [
    { title: 'Starter',
      price: 'Free',
      color: 'grey',
      time: 'Forever',
      features: [
        '3 Figma and 3 FigJam files',
        'Unlimited personal files',
        'Unlimited collaborators',
        'Plugins and templates',
        'Mobile app',
        'Music player',
        'Ready-made templates',
      ]
      },
      { title: 'Figma Professional',
      price: '$12 per editor/month',
      color: 'green',
      time: 'Forever',
      features: [
        'Unlimited Figma files',
        'Unlimited version history',
        'Sharing permissions',
        'Shared and private projects',
        'Team libraries',
        'Audio conversations',
    
      ]
      },
      { title: 'Figma Organization',
      price: '$45 per editor/month',
      color: 'blue',
      time: 'Forever',
      features: [
        'Org-wide libraries',
        'Design system analytics',
        'Branching and merging',
        'Centralized file management',
        'Unified admin and billing',
        'Private plugins and widgets',
        'Single sign-on',
      ]
      },
    ],
    ]
  };
},
  methods: {
    onSelectType (type) {
      this.type = type;
    }
  }
}
</script>

<style scoped>
.cards-grid {
  display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
    margin: 64px auto 40px;
}
</style>
