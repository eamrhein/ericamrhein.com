<script>
  import GoogleAnalytics from "sapper-google-analytics/GoogleAnalytics.svelte"
  import { stores } from "@sapper/app"

  let ga_measurment_id = "UA-252042200"  // your analytics id
</script>

<GoogleAnalytics {stores} id={ga_measurment_id}/>
<main>
  <slot />
</main>
