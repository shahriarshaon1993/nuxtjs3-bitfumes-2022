<template>
    <div>

        <Head>
            <Title>Nuxt3 - iPhone {{ name }}</Title>
        </Head>
        <div class="flex justify-center w-full mt-20">
            <div class="grid grid-cols-2">
                <div>
                    <img src="/images/iphn12.jpg" width="200"/>
                </div>
                <div class="text-center">
                    <h1 class="text-3xl">Iphone {{ name }}</h1>
                    <button @click="addToCart" class="p-3 bg-indigo-900 text-white rounded-md mt-5 w-48">
                        <span v-if="isInCart()">Remove from Cart </span>
                        <span v-else>Buy Now </span>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const route = useRoute();
    const cart = useCart();

    const name = computed(() => {
        return route.params.name;
    });

    const fullname = computed(() => {
        return `iphone-${route.params.name}`;
    });

    function isInCart() {
        return !!cart.value.find((ct) => ct.name === fullname.value);
    };

    function addToCart() {
        if(!isInCart( )) {
            cart.value.push({name: fullname});
        }else {
            cart.value = cart.value.filter((ct) => ct.name !== fullname.value);
        }
    }

    // useHead({
    //     title: `Nuxt3 - iPhone ${route.params.name}`
    // });
</script>