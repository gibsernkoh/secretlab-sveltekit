<script lang="ts">
     import Placeholder from "$lib/components/Placeholder.svelte"
     import DropdownShopNow from "./Dropdown/ShopNow.svelte"

     const items = [
          { href: '/collections'              , title: 'Shop Now'     , Dropdown: DropdownShopNow  },
          { href: '/collections/gaming-chairs', title: 'Chairs'},
          { href: '/collections/gaming-chairs', title: 'Desks'},
          { href: '/collections/gaming-chairs', title: 'Accessories'},
          { href: '/collections/gaming-chairs', title: 'Info'},
          { href: '/collections/gaming-chairs', title: 'Technology'},
     ]
</script>

<header>
     <div class="container mx-auto flex items-center justify-between py-2">
          <a href='/' title='Home Page'>
               <Placeholder width={88} height={22} alt="Logo" />
          </a>
          
          <div class='flex gap-4'>
               {#each items as { href, title, Dropdown } }
                    <div class="relative group">
                         <a href={href} title={title}>{title}</a>
                         {#if Dropdown }
                              <Dropdown />
                         {/if}
                    </div>
               {/each}
          </div>

          <div class="flex gap-4 text-lg">
               <iconify-icon icon="ph:magnifying-glass-bold"></iconify-icon>
               <iconify-icon icon="ph:shopping-cart-fill"></iconify-icon>
          </div>
     </div>
</header>
