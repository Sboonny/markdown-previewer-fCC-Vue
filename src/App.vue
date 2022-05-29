<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: "Markdown",
  data() {
    return {
      markdownPlaceholder: `# Welcome to my Vue Markdown Previewer!

## This is a sub-heading...
### And here's some other cool stuff:

Here's some code, \`< div > </div>\`, between 2 backticks.

          \`\`\`
// this is multi-line code:

function anotherExample(firstLine, lastLine) {
  if (firstLine == '\`\`\`' && lastLine == '\`\`\`') {
    return multiLineCode;
  }
}
\`\`\`

You can also make text ** bold **...whoa!
Or _italic_.
    Or...wait for it... ** _both!_**
  And feel free to go crazy ~~crossing stuff out~~.

    There's also [links](https://www.freecodecamp.org), and
> Block Quotes!

And if you want to get really crazy, even tables:

Wild Header | Crazy Header | Another Header ?
  ------------ | ------------- | -------------
    Your content can | be here, and it | can be here....
And here. | Okay. | I think we get it.

- And of course there are lists.
  - Some are bulleted.
     - With different indentation levels.
        - That look like this.


1. And there are numbered lists too.
1. Use just 1s if you want!
1. And last but not least, let's not forget embedded images:

![freeCodeCamp Logo](https://cdn.freecodecamp.org/testable-projects-fcc/images/fcc_secondary.svg)
  `
    }
  },
  mounted() {
    this.markdownPlaceholder
  }
}) 
</script>

<template>
  <main>
    <form>
      <label for="editor">Markdown-Editor:</label>

      <textarea id="editor" name="markdown-editor" spellcheck="true">{{ markdownPlaceholder }}
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
