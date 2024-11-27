<script>
 import { openModal } from "../store";
 

</script>
 <header class="flex flex-col relative z-20">
<div class="max-w-wdith-[1400px] mx-auto w-full flex items-center justify-between
p-4 py-6" >
<a href="/">
<h1 class="font-semibold" >Prime <span class="text-indigo-400">Patek</span></h1>

</a>
<button  on:click={() => ($openModal = true)} class="md:hidden grid place-items-center">
<i class="fa-solid fa-bars"></i>
</button>
<nav class=" hidden md:flex items-center gap-4 lg:gap-6">
    <a href="#product"  class="duration-200 hover:text-indigo-400 cursor-pointer">Products & Services</a>
    <a href="#reviews" class="duration-200 hover:text-indigo-400 cursor-pointer">Reviews</a>
    <a href="#faq" class="duration-200 hover:text-indigo-400 cursor-pointer">FAQs</a>
<button class="Specialbtn">
<p>Contact Us Now </p>

</button>

</nav>



</div>


<script src="https://static.elfsight.com/platform/platform.js" async></script>
<div class="elfsight-app-93aaeba1-5ed6-4a07-9131-b002faa21ada" data-elfsight-app-lazy></div>
 </header>