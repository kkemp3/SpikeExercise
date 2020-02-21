<template>
  <div>
    <h1>All About Me</h1>
      <table>
      <tr>
        <td width="75%" valign="top">
          <p>
            I am a 4th year student here at UW-Madison majoring in Computer Science. I like to play and watch hockey, pet dogs, and drink craft beers.
          </p>
        </td>
        <td align="right">
          <AboutNav />
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import AboutNav from '@/components/AboutNav'
export default {
  components: {
    AboutNav
  }
}
</script>

<style>
h1 {
  font-family: sans-serif;
  padding: 5px 5px 5px 5px;
  text-align: center;
}
</style>
