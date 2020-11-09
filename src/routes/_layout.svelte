<script>
  import GoogleAnalytics from "sapper-google-analytics/GoogleAnalytics.svelte"
  import { stores } from "@sapper/app"

  let ga_measurment_id = "G-7G7ZJJT10C"  // your analytics id
</script>

<GoogleAnalytics {stores} id={ga_measurment_id}/>
<main>
  <slot />
</main>
