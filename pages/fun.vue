<template>
  <div>
    <h1>Fun Stuff</h1>
    <table>
      <tr>
        <td width="75%" valign="top">
          <p>
            I am working on an app that allows users to post pictures of their food when they go to restaurants so that other's can see what their food may look like
            before deciding on ordering them.
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
