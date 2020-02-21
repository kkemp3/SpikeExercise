<template>
  <div>
    <h1>Fun page</h1>
      <table>
      <tr>
        <td width="75%" valign="top">
          <p>
            I want to make a zillion dollars.
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
