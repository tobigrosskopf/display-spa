<script>
import { name } from '../store.js'
import _ from 'lodash'

const cards = _.range(30).map(x => 'Item No ' + String(x))


function showCard(card) {
    console.log(card)
    name.update(x => card)
}
</script>

<!-- Always shows a header, even in smaller screens. -->
<div class="mdl-layout mdl-js-layout mdl-layout--fixed-header">
  <header class="mdl-layout__header">
    <div class="mdl-layout__header-row">
      <!-- Title -->
      <span class="mdl-layout-title">Projects</span>
    </div>
  </header>
  <div class="mdl-layout__drawer">
    <span class="mdl-layout-title">Projects</span>
    <nav class="mdl-navigation">
    {#each cards as card}
      <div class="mdl-navigation__link" on:click={() => showCard(card)}>{card}</div>
    {/each}
    </nav>
  </div>
  <main class="mdl-layout__content">
    <div class="page-content"><!-- Your content goes here --></div>
  </main>
</div>