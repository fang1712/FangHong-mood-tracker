<script>
    import supabase from '$lib/db';
import Login from '$lib/login.svelte';
import Signup from '$lib/signup.svelte';
    

    async function logout() {
   	 const { error } = await supabase.auth.signOut();

   	 if (error) alert(error.message); // alert if error
    }

</script>

<!-- Sign Out -->
<section class="container px-4 py-3 text-center">
    <button class="btn btn-secondary" on:click={logout}>Logout</button>
</section>	

<Signup/>
<Login/>