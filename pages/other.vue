<template>
  <div>
    <h1>Other Stuff</h1>
     <table>
      <tr>
        <td width="75%" valign="top">
          <p>
            Some other stuff.
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
