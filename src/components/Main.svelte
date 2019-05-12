<script>
import { name } from '../store.js'

let name_value;

const unsubscribe = name.subscribe(value => {
    name_value = value;
});
    
</script>

<div style="height: 10vh;"></div>

<div class="mdl-grid">
    <!-- <div class="mdl-cell mdl-cell--12-col"> -->

        <div class="demo-card-event mdl-card mdl-shadow--2dp mdl-cell mdl-cell--12-col">
        <div class="mdl-card__title mdl-card--expand">
            <h4>
                {name_value}
            </h4>
        </div>

        </div>

    <!-- </div> -->
</div>

