<script>
    const lgTextClass = "xl:text-7xl xl:leading-[74px] lg:text-6xl lg:leading-[60px] md:text-5xl md:leading-[56px] sm:text-[44px] sm:leading-[50px] xsText "

    let isHovered = false;
</script>
    
    <div id='bgCont' class="bg-[url(/A11yImage.png)] bg-cover bg-center bg-no-repeat w-full h-[80vh] flex justify-center items-center" alt="A11y Accessibility Image">
        <div id="HeroCont" class='h-2/3 w-[80vw] flex justify-center items-center relative'>
            <div class="h-full w-full absolute bg-white opacity-90 rounded-xl"></div>
            <div id="textCont" class='flex flex-col w-full h-full justify-around items-center gap-2 p-4 lg:p-8 relative'>
                <div class={lgTextClass + "text-start"}>
                    “98% of U.S.-based webpages are not accessible to the disability community from a legal perspective…”
                </div>
                <div class="w-full lg:text-3xl md:text-2xl text-xl italic text-wrap">
                    - 2020 Web Accessibility Annual Report
                </div>
                <div
                    class="flex flex-row w-fit justify-center items-center text-white"
                    role="button"
                    tabindex=0
                    on:mouseenter={() => isHovered = true}
                    on:mouseleave={() => isHovered = false}
                >
                <a href='#WhySvARIA'>
                    <div class="flex flex-row">
                        <div class={"lg:text-4xl md:text-3xl sm:text-2xl text-xl font-bold bg-[#04abdb] px-4 py-2 rounded-3xl border-2 border-[#143d66] opacity-90 hover:contrast-150 hover:opacity-100"}>
                            <span class:animate-wiggleSm-hover={isHovered}>SvARIA</span> can help.
                        </div>
                    </div>
                    </a>
                </div>
            </div>
        </div>
    </div>