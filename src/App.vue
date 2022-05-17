<script setup lang="ts">

</script>

<template>
  <main>
    <form>
      <label for="editor">Markdown-Editor:</label>

      <textarea id="editor" name="markdown-editor" spellcheck="true">
</textarea>
      <label for="previewer">Markdown-Previwer:</label>

      <textarea id="previewer" name="markdown-previewer" readonly></textarea>

    </form>

  </main>
</template>

<style>
*,
*::after,
*::before {
  box-sizing: border-box;
}

main form {
  font-family: Arial, Helvetica, sans-serif;
  display: flex;
  gap: .5em;
}

main form label {
  font-weight: 800;
  letter-spacing: 2px;
}

main form textarea {
  width: 50%;
  height: 90vh;
}
</style>
