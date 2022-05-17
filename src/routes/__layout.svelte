<script>
    import "../app.css";
    import Nav from '../components/nav.svelte'
  </script>
<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
</svelte:head>

<div class="bg-blue-200 h-full">
  <div class="content p-8 max-w-6xl mx-auto bg-blue-200">
    <Nav/>
    <slot />
  </div>
</div>