<template>
  <div>
  <h1>Classes page</h1>
    <table>
      <tr>
        <td width="75%" valign="top">
          <p>
            <ul>
              <li>CLASSICS340: Conspiracy in the Ancient and Modern Worlds</li>
              <li>COMARTS260: Communication and Human Behavior</li>
              <li>COMPSCI559: Software Engineering</li>
              <li>GEOG340: World Regions in Global Contextr</li>
              <li>INTER-LS210: LS Career Development: Taking Initiative</li>
            </ul>
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
th, td {
  padding: 15px
}
</style>
