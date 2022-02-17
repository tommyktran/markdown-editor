<script>
    // @ts-nocheck
    
      import { Editor } from '../../node_modules/bytemd';
      import gfm from '../../node_modules/@bytemd/plugin-gfm/lib/index';
    
      import { onMount } from 'svelte'
      let value = '';
      const plugins = [
        gfm(),
        // Add more plugins here
      ];
    
      function handleChange(e) {
        value = e.detail.value;
      }
    </script>
    
    <template>
      <Editor {value} {plugins} on:change={handleChange} />
    </template>
    
    <style>
        @import '../../node_modules/bytemd/dist/index.min.css';
    </style>