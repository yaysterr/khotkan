<script>
    let imageSrc1 = "doll-front.webp";
    let imageSrc2 = "jersey-front.png";
    let name = '';
    let size = '';
    let className = '';
</script>

<style>
    img {
        transition: opacity 0.5s ease-in-out, transform 0.3s ease-in-out;
    }
    img:hover {
        transform: scale(1.05);
    }
</style>
<div class="flex flex-col items-center justify-center h-screen">
    <div class="">
        <a href="https://www.instagram.com/kanwgemo/" >
            <img
                class="w-32 h-auto cursor-pointer"
                src={imageSrc1}
                alt=""
                on:mouseenter={() => (imageSrc1 = "doll-back.webp")}
                on:mouseleave={() => (imageSrc1 = "doll-front.webp")}
            />
        </a>
    </div>
    <div class="flex flex-col items-center justify-center ">
        <p>New Collection</p>
        <p>↓</p>
    </div>
</div>
<div class="mt-10 w-screen h-screen">
    <div class="flex flex-col items-center justify-center">
            <img
                class="w-xl h-auto cursor-pointer" 
                src={imageSrc2}
                alt=""
                on:mouseenter={() => (imageSrc2 = "jersey-back.png")}
                on:mouseleave={() => (imageSrc2 = "jersey-front.png")}
            />
    </div>
    <div class="flex flex-col items-center justify-center">
        <p class="text-gray-400 mt-10">You want this for a Farewell's souvenir?</p>
        <input
            type="text"
            bind:value={name}
            placeholder="Enter your name"
            class="text-center mt-3 px-4 py-2 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
            on:focus={() => name === '' && (event.target.placeholder = '')}
            on:blur={() => name === '' && (event.target.placeholder = 'Enter your name')}
        />
        <input
            type="text"
            bind:value={className}
            placeholder="Enter your class"
            class="text-center mt-3 px-4 py-2 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
            on:focus={() => className === '' && (event.target.placeholder = '')}
            on:blur={() => className === '' && (event.target.placeholder = 'Enter your class')}
        />
        <input
            type="text"
            bind:value={size}
            placeholder="Enter your size(s,m,l,xl)"
            class="text-center mt-3 px-4 py-2 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
            on:focus={() => size === '' && (event.target.placeholder = '')}
            on:blur={() => size === '' && (event.target.placeholder = 'Enter your size(s,m,l,xl)')}
        />
    </div>
    <div class="flex flex-col items-center justify-center">
        <button 
        class="cursor-pointer mt-20 px-6 py-2 bg-[#ddff00] text-black font-semibold rounded-full shadow-md hover:bg-[#99ff00] focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 transition-transform transform hover:scale-105">
        Reserve
        </button>
    </div>
</div>
