<script lang="ts">
  export let name: string = "Foo"
  export let nickname: string = ""
  export let phone: string = ""
  export let email: string = ""
  export let github: string = ""
  export let linkedin: string = ""
  export let location: string = ""
  export let website: string = ""
</script>

<div>
  <h2
    class="flex-none order-first sm:order-none print:order-none text-4xl sm:text-2xl md:text-3xl lg:text-6xl text-center p-4 print:pt-0"
  >
    {name}
    <span class="block -mt-1 text-base lg:text-lg">({nickname})</span>
  </h2>
  <p>
    <a href={`tel:${phone}`}>{phone}</a> | <a href={`mailto:${email}`}>{email}</a> | {location} | 
    <a href={`https://github.com/${github}`} target="_blank" rel="noreferrer">
      github.com/{github}
    </a> |
    <a href={`https://linkedin.com/in/${linkedin}`}
        target="_blank"
        rel="noreferrer">linkedin.com/{linkedin}</a>
  </p>
</div>

<style>
  a {
    text-decoration: underline;
  }

  @media print {
    h1 {
      @apply text-3xl;
    }
  }
</style>
