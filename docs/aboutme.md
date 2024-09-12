---
layout: doc
---

<script setup>
  import {data as aboutme} from './aboutme/aboutme.data';
  import { withBase } from 'vitepress';
</script>

# Blogs

<ul v-if="aboutme.length > 0">
  <li v-for="aboutme of aboutme">
    <a :href="withBase(aboutme.url)">{{ aboutme.frontmatter.title }}</a>
  </li>
</ul>
<p v-else>
  Nothing here yet!
</p>
