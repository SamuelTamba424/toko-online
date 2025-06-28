<template>
  <q-layout view="hHh lpR fFf">
    <!-- Navbar -->
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title class="text-h6 text-weight-bold">
          🛒 Toko Online
        </q-toolbar-title>
        <q-btn flat label="Beranda" />
        <q-btn flat label="Produk" />
        <q-btn flat label="Kontak" />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- Footer -->
    <q-footer class="bg-grey-9 text-white text-center q-pa-md">
      &copy; 2025 TokoKu. Semua Hak Dilindungi.
    </q-footer>
  </q-layout>
</template>

<script setup>
// kosong karena tidak perlu logic untuk layout dasar
</script>
