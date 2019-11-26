<template>
  <q-page class="flex flex-center">
    <img alt="Quasar logo" src="~assets/quasar-logo-full.svg">
    hello

    <svg id="svgLogo1" width="400" height="400" viewBox="0 0 400 400" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <defs>
        <!-- a transparent grey drop-shadow that blends with the background colour -->
        <filter id="shadow" width="1.5" height="1.5" x="-.25" y="-.25">
          <feGaussianBlur in="SourceAlpha" stdDeviation="2.5" result="blur"/>
          <feColorMatrix result="bluralpha" type="matrix" values=
              "1 0 0 0   0
              0 1 0 0   0
              0 0 1 0   0
              0 0 0 0.4 0 "
          />
          <feOffset in="bluralpha" dx="3" dy="3" result="offsetBlur"/>
          <feMerge>
            <feMergeNode in="offsetBlur"/>
            <feMergeNode in="SourceGraphic"/>
          </feMerge>
        </filter>

        <!-- a transparent grey glow with no offset -->
        <filter id="black-glow">
          <feColorMatrix type="matrix" values=
              "0 0 0 0   0
              0 0 0 0   0
              0 0 0 0   0
              0 0 0 0.7 0"
          />
          <feGaussianBlur stdDeviation="2.5" result="coloredBlur"/>
          <feMerge>
            <feMergeNode in="coloredBlur"/>
            <feMergeNode in="SourceGraphic"/>
          </feMerge>
        </filter>

        <!-- a transparent glow that takes on the colour of the object it's applied to -->
        <filter id="glow">
          <feGaussianBlur stdDeviation="2.5" result="coloredBlur"/>
          <feMerge>
            <feMergeNode in="coloredBlur"/>
            <feMergeNode in="SourceGraphic"/>
          </feMerge>
        </filter>

        <filter id="glow2">
          <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
          <feMerge>
            <feMergeNode in="coloredBlur"/>
            <feMergeNode in="coloredBlur"/>
            <feMergeNode in="coloredBlur"/>
            <feMergeNode in="SourceGraphic"/>
          </feMerge>
        </filter>
      </defs>

      <g transform="translate(20,20)">
        <path transform="translate(90,20)" d="M0,0L10,10L20,0L30,10" stroke="black"
        filter="url(#shadow)" stroke-width="3" fill="none"/>
        <path transform="translate(90,70)" d="M0,0L10,10L20,0L30,10" stroke="#d00"
        filter="url(#black-glow)" stroke-width="3" fill="none"/>
        <path transform="translate(90,120)" d="M0,0L10,10L20,0L30,10" stroke="#d00"
        filter="url(#glow)" stroke-width="3" fill="none"/>

        <path transform="translate(90,120)" d="M0,0L10,10L20,0L30,10" stroke="#d00"
        filter="url(#glow2)" stroke-width="3" fill="none"/>

        <path class="exampleGlow" d="M100,250 C100,100 400,100 400,250" style="fill-opacity: 0; stroke-width: 2; stroke: red; filter: url(#glow2);" transform="translate(-250,-200)"/>
      </g>

    </svg>

  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex'
}
</script>
