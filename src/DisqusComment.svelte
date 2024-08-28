<script lang="ts">
	import { onMount } from "svelte";

  export let url: string;
  export let identifier: string;
  export let shortName: string;
  export let title: string = '';
  export let theme: 'light' | 'dark' = 'light'; 

  onMount(() => {
    const cfgScript = document.createElement('script');
    cfgScript.id = 'disqus_config_section';
    cfgScript.type = 'text/javascript';
    cfgScript.text = `var disqus_config = function () {
      this.page.title = '${title}';
      this.page.url = '${url}';
      this.page.identifier = '${identifier}';
    };`;
    document.body.appendChild(cfgScript);

    (function() { // DON'T EDIT BELOW THIS LINE
      var d = document, s = d.createElement('script');
      s.src = `https://${shortName}.disqus.com/embed.js`;
      s.setAttribute('data-timestamp', `${+new Date()}`);
      (d.head || d.body).appendChild(s);
    })();
  })
</script>

<div id="disqus_thread" style="color-scheme: {theme};"></div>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
