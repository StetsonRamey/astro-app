<script>
  export let content;
</script>

<div class="card">
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
</style>
