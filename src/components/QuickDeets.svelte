<script>
  export let content;
  import * as tools from "../../public/toolData.json";

  const projects = Object.keys(tools.default)
  const tool = projects.find(t => t === content.title)
  const used = tools.default[tool]
</script>

<div class="card">
  <p><strong>Site:</strong></p>
  <p><a href="{content.site}">{content.site}</a></p>
  <p><strong>Tools:</strong></p>
    <ul class="pl2">
      {#each used as t}
        <li class="tools"><a href="{t.url}">{t.name}</a></li>
      {/each}
    </ul>
  <p><strong>Stack:</strong></p>
  <p>{content.stack}</p>
  <p><strong>Purpose:</strong></p>
  <p>{content.purpose}</p>
  <p><strong>Backend:</strong></p>
  <p>{content.backend}</p>
</div>

<style>
  .card {
    display: grid;
    grid-template-columns: 12% 88%;
  }
  a {
    color: var(--c-black);
    cursor: default;
  }
  a:hover {
    color: var(--c-green);
  }
</style>
