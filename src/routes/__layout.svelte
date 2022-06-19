<!-- This is where we put the consistent parts of the layout (Nav, footer) -->
<script>
	import '../app.css';
	import '../styles.css';
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<Nav />
<!--must include slot for page content -->
<slot />
<Footer />
