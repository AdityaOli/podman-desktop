<script lang="ts">
import type { CatalogExtensionInfoUI } from './catalog-extension-info-ui';
import CatalogExtension from './CatalogExtension.svelte';

export let catalogExtensions: CatalogExtensionInfoUI[];
</script>

<div class="flex flex-col grow p-4">
  {#if catalogExtensions.length > 0}
    <div class="pb-4">Available extensions</div>
  {/if}

  <div class="flex flex-col w-full">
    <div
      class="grid min-[920px]:grid-cols-2 min-[1180px]:grid-cols-3 gap-3"
      role="region"
      aria-label="Catalog Extensions">
      {#each catalogExtensions as catalogExtension}
        <CatalogExtension catalogExtensionUI="{catalogExtension}" />
      {/each}
    </div>
  </div>
</div>
