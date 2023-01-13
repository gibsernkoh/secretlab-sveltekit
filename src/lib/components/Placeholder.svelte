<script lang="ts">
     let className = 'inline-block'
     export { className as class }

     export let width = 100
     export let height
     export let alt

     let src=`https://via.placeholder.com/${width}`

     if (!!height)
          src += `x${height}.png`
</script>

<img src={src} alt={alt} class={className} />