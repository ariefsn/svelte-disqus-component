# Svelte Disqus Component

This package is for integrating [Disqus](https://disqus.com) to Svelte application.

## How to

1. Install

    ```shell
    npm install svelte-disqus-component
    // or
    yarn add svelte-disqus-component
    ```

2. Import

    ```typescript
    import DisqusComment from 'svelte-disqus-component/src/DisqusComment.svelte';
    import DisqusCount from 'svelte-disqus-component/src/DisqusCount.svelte';
    ```

3. Use it

    ```html
    <script>
      const shortName = 'disqus-shortname'
      const url = 'https://some-url'
      const id = 'some-id'
      const title = 'The Title'
    </script>

    <DisqusComment {shortName} {url} identifier={id} {title}/>
    <DisqusCount {shortName} />
    ```

4. Props

  | Name  | Description  | Required | Default  |
  |---|---|---|---|
  | `shortName`  | Disqus shortname  | Yes |   |
  | `url` | URL of the content | Yes  |  |
  | `identifier` | The content's identifier | Yes  |  |
  | `title` | The content's title | No  | `undefined` |
