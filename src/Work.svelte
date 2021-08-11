<script lang="ts">
  import HideToggle from "./HideToggle.svelte"

  export let position: string = ""
  export let company: string = ""
  export let url: string = ""
  export let years: string[] = []
  export let details: string[] = []
</script>

<div class="work-experience">
  <HideToggle />
  <div class="flex flex-col font-bold mb-2 print:mb-1 sm:flex-row">
    <div class="flex-1 text-left">{position} <span class="hidden sm:inline">-</span> <a href={url} target="_blank" rel="noreferrer" class="block sm:inline">{company}</a></div>
    <div class="flex-0 text-left sm:text-right">{years.join(" - ")}</div>
  </div>
  <ul class="text-left list-disc pl-8 print:pl-6">
    {#each details as detail}
      <li>
        <HideToggle />
        {detail}
      </li>
    {/each}
  </ul>
</div>

<style>
  .work-experience {
    @apply my-4;
  }

  a {
    text-decoration: underline;
    font-size: 14px;
    font-weight: normal;
    color: #616161;
  }

  @media print {
    .work-experience {
      @apply my-1;
    }
  }
</style>
