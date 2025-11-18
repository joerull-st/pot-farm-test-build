<!-- 
@component
### Subhead component
Renders an h2 tag in the style of the Immersive Template.  
Wrap this component around the markup you want rendered.

#### Example
```svelte
<Subhead>Hello world!</Subhead>
```
-->

<script>
  /** @type {{children?: function}} */
  let { children } = $props();
</script>

<h2 class="font-editorial-article-header-02 text-text-primary text-[1.85rem] pt-8">
  {@render children?.()}
</h2>
