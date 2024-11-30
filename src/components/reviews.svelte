<script>
    import ReviewCard from "./reviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./stars.svelte";

    let lim = true;

    let reviewsList = [
        {
            name: "John Uche",
            review: "i've been having issues with my printers, i called them and they came quickly to get it fixed, it's working perfectly now",
            
            
            features: [
                "servicing my machine",
                "Quality toners ",
                "speed ",

            ],
        },
        {
            name: "John chinedu",
            review: " I called 5 engineers, and none of them was able to remove an error code my machine was showing.That was allowing it not to print,Prime Patek sent over an engineer, and just after 30 minutes, he got it fixed",
            features: [
                "Excellent engineers",
                "Quality toners ",
                "Nice Pricing",
            ],
        },
        {
            name: "Michael Brown",
            review: "Getting services form prime patek has been one of my best investments so far, they are very reliable and i can vouche that",
            features: [
                "Right on Time ",
                "Expert Engineers ",
                "Quality machines",
            ],
        },
        {
            name: "Sarah Williams",
            review: "I'm a single mom of two, Running a Business can be so frustrating knowing the services i get from prime patek alwyas reduce the stress and i can always rely on them   ",
            features: [
                "Expert Engineers",
                "Quality machines",
            
            ],
        },
        {
            name: "David ",
            review: "I was Always changing engineers until my friend referred me to them and I've never changed since then ",
            features: [
                "Quality parts",
                "Very Nice Engineers",
                "Detailed data analysis",
            ],
        },
        {
            name: "isarel Adeniyi ",
            review: "Tho they where not cheap to me, But my money was spent well, They offer the best services out there the marketplace",
            features: [
                "Right on Time",
                "Quality products",
                "Detailed explanation",
            ],
        },
        {
            name: " George ",
            review: "I've never been in a situation where I'm in need of toners for a job and prime patek has'nt gotten me one",
            features: [
                "Good Engineers  ",
                "Quality parts ",
                
            ],
        },
    ];
</script>

<SectionWrapper id="reviews">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Don't just take our word for it
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                See What <span class="text-indigo-400">Others</span> Have To Say
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index} />
                {/each}
            </div>
        </div>
        <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Show More" : "Show Less"}</p>
        </button>
        <div class="flex flex-col gap-10">
            <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
                Trusted by 500 printing companies 
            </p>
            <Stars/>

        </div>
    </div>
</SectionWrapper>