<script lang="ts">
	import { onMount } from "svelte";

  export let shortName: string;

  onMount(() => {
    const countScript = document.createElement('script');
    countScript.id = 'dsq-count-scr';
    countScript.type = 'text/javascript';
    countScript.src = `https://${shortName}.disqus.com/count.js`;
    document.body.appendChild(countScript);
  })
</script>
