<template>
  <div>
    <!-- <Menu />
    <Toast
      :breakpoints="{ '920px': { width: '100%', right: '0', left: '0' } }"
    ></Toast> -->

    <div id="main" class="">
      <Nuxt />
    </div>
    <nav id="navbar" class="navbar">
      <ul class="navbar-nav">
        <li class="logo">
          <a href="#" class="nav-link">
            <i class="fa fa-pastafarianism"></i>
            <span class="link-text logo-text">Home</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link fa-primary">
            <i class="fas fa-glass-martini"></i>
            <span class="link-text">Link1</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link fa-primary">
            <i class="fas fa-glass-martini"></i>
            <span class="link-text">Link1</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link fa-primary">
            <i class="fa fa-sliders-h"></i>
            <span class="link-text">Settings</span>
          </a>
        </li>
      </ul>
    </nav>

    <footer>Footer</footer>
  </div>
</template>

<script>
// import Menu from '@/components/Menu'
export default {
  components: {
    // Menu,
  },
  data() {
    return {
      ts: [],
      menuItems: [
        {
          label: 'Home',
          icon: 'pi pi-fw pi-file',
          items: [],
        },
        {
          label: 'Edit',
          icon: 'pi pi-fw pi-pencil',
          items: [
            {
              label: 'Left',
              icon: 'pi pi-fw pi-align-left',
            },
            {
              label: 'Right',
              icon: 'pi pi-fw pi-align-right',
            },
            {
              label: 'Center',
              icon: 'pi pi-fw pi-align-center',
            },
            {
              label: 'Justify',
              icon: 'pi pi-fw pi-align-justify',
            },
          ],
        },
      ],
    }
  },
}
</script>
<style scoped>
#main {
  margin-left: 200px;
}
</style>
