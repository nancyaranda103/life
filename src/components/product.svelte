<script>
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: [
                "Daily streak counter",
                "Get one year free grauntee on any purchase",
                "Community challenges",
                "Every workout is new and exciting",
            ],
            description:
                "prime patek sells the best machine that fits your printing needs e.g bizub, sharp, konaca monica, tested to make sure its fully working before sending off",
            imgUrl: "assets/machine 1.jpg",
        },
        {
            featureList: [
                "Select your preferences",
                "Personalize your workouts",
                "Customize your training",
                "Guarantees progress on all core exercises",
            ],
            description:
                "With our experienced engineers we fill find the best way and cost effective way to make your machine work again ",
            imgUrl: "assets/machine 2.jpg",
        },
        {
            featureList: [
                "Eliminating guesswork",
                "Save time",
                "Achieve the performance you seek",
                "Builds functional strength",
            ],
            description:
                "Enter as much information about yourself as you desire to ensure all workouts are personalized to your every need.",
            imgUrl: "assets/machine 3.jpg",
        },
    ];
</script>

<SectionWrapper id="product">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                call us for servicing your <span class="text-indigo-400"
                    > machine </span
                > today
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
              Our Services 
            </h3>
        </div>

        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                    Experience ease of  <span
                        class="text-indigo-500 font-medium">purchasing</span
                    > and buying machines
                {:else if index === 1}
                    Repair and <span
                        class="text-indigo-400 font-medium">service </span
                    > old and damaged machines
                {:else}
                    Workouts specific to your <span
                        class="text-indigo-400 font-medium">environment</span
                    >
                    and
                    <span class="text-indigo-400 font-medium">expertise</span>
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>