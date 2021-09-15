<template>
  <div>
    <header>
      <div class="logo">
        <svg width="130" height="130" viewBox="0 0 130 130" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" clip-rule="evenodd" d="M65 129C100.346 129 129 100.346 129 65C129 29.6538 100.346 1 65 1C29.6538 1 1 29.6538 1 65C1 100.346 29.6538 129 65 129ZM59.9728 36.6725H59.7767H30.7268V54.013H48.0153V62.6703L49.321 64.3034L49.5042 64.5312L49.6874 64.7589L56.5306 73.3153L61.7946 79.8944L68.1113 87.7882L68.2945 88.0185L68.4778 88.2463L68.6274 88.4352L73.8191 94.9237L79.785 102.38L79.9501 102.587L80.1153 102.794L82.3344 105.569V79.8426L81.0107 78.1888L80.8275 77.961L80.6442 77.7307L73.8191 69.1976L68.5036 62.5538L62.1945 54.6678L62.0113 54.4375L61.8281 54.2097L61.6707 54.013H99.6229V36.6725H68.181H59.9728Z" fill="#FF2156" />
        </svg>
      </div>
      <nav>
        <ul>
          <li>
            <NuxtLink to="/">
              Home
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/login">
              Login
            </NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
    <main>
      <Nuxt />
    </main>
    <footer>
      <div class="creators">
        Designed by <a href="https://www.puylaertpaco.com/">Fuxia</a> X Implemented by <a href="https://harambasic.de">Luka Harambasic</a>
      </div>
      <div class="techno">
        Techno 2k21
      </div>
    </footer>
  </div>
</template>

<style lang="sass">
@import url('https://fonts.googleapis.com/css2?family=Spartan:wght@400;700&display=swap')
@import 'assets/reset.sass'

body
  color: #202020 // TODO css
  font-family: 'Spartan', sans-serif // TODO css
  background: #f8f8f8 // TODO css
  margin: 4rem // TODO replace
  line-height: 1.75
</style>
