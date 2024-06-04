<script global>
    import '../global.css'
    import jeep1 from '$lib/assets/jeep1.jpg';
    import * as HoverCard from '$lib/components/ui/hover-card/index.ts';
	import * as Dialog from '$lib/components/ui/dialog/index.ts';
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Manrope:wght@400;600;800&display=swap');

    main {
        font-family: 'Manrope', sans-serif;
    }
    .shadowed-text {
        text-shadow: 4px 4px 6px rgba(0, 0, 0, 0.7);
    }
    video { 
        position: absolute;
        top: 0;
        right: 0;
        min-width: 100%;
        max-height: 30vh;
        width: auto;
        height: auto;
        z-index: -1;
        /* to change the blur effect edit the number below in your code*/
        filter:blur(4px);
    }
</style>

<main>
    <section
    class="relative w-full h-[30vh] "
	>
        <video class= "absolute w-full h-full object-cover -z-10"muted autoplay loop playsinline disablepictureinpicture>
            <source src="baguiodrive.mp4" type="video/mp4" />
        </video>
            
        <div
			class="shadowed-text min-h-screen-minus-navbar mx-auto flex max-w-6xl flex-col items-center justify-center gap-2 py-16 pt-12 text-center"
		>
			<h1 class="text-blue-500 leading-1.1 text-3xl font-bold tracking-tighter drop-shadow-xl sm:text-6xl">
				#Jeepney<span class="decoration-red-800 text-white text-muted line-through decoration-destructive decoration-wavy"
					>Moder</span
				>N<span class="decoration-red-800 text-muted line-through decoration-destructive decoration-wavy text-white">iz</span
				>ation
			</h1>
			<h1
				class="text-blue-500 leading-1.1 text-2xl font-bold tracking-tighter  drop-shadow-lg sm:text-5xl"
			>
				Gumagana ang Tigil-Pasada.
			</h1>
			<p class="max-w-[350px ]text-sm mb-6 font-bold sm:max-w-[750px] text-white sm:text-lg">
				Op-Ed ni Caleb Bunye
			</p>
        </div>
    </section>
    <section
		class="mx-auto flex h-screen flex-col items-center justify-center gap-2 py-20 text-center"
	>
		<div
			class="absolute z-10 h-screen-minus-navbar w-full bg-jeep2 bg-cover bg-center opacity-30 blur-sm"
		></div>

		<p
			class="text-justify z-20 mx-16 max-w-[850px] text-2xl font-medium leading-tight hover:drop-shadow-2xl md:text-3xl [&:not(:first-child)]:mt-6"
		>
        Noong 2014 naglabas ng pag-aaral ang Japan International Cooperation Agency (JICA) na napag-alamang nakakaltasan tayo ng P2.4 bilyon kada araw dahil sa trapiko (JICA). Bilang pagtugon sa suliraning ito, noong June 19, 2017, naglabas ng bagong programa ang Department of Transportation o DOTr na naglalayong pagandahin at gawing mas moderno ang mga pampublikong sasakyan at agapan ang lumalaking problema sa trapik. Ang programang ito’y mas kilala bilang Jeepney Modernization Program (JMP) na sumasailalim sa  

			<span
				class="font-bold underline decoration-primary/80 decoration-4 duration-200 ease-in hover:text-primary hover:decoration-transparent"
				>Public Utility Vehicle  Modernization Program o PUVMP (LTFRB).
            </span>
		</p>
	</section>
    <section
		class="mx-auto flex h-full max-w-6xl grid-cols-2 flex-col items-center gap-8 px-4 py-20 md:grid md:h-screen md:gap-16"
		id="overview"
	>
		<div>
                <h1
                    class="font-jeepney text-8xl font-extrabold tracking-tight text-blue-500 drop-shadow-md"
                >
                    01
                </h1>
                <h1 class="font-jeep text-7xl uppercase tracking-tight text-blue-500 drop-shadow-lg">
                    Overview
                </h1>
                <p class="mt-6 text-lg">
                        Ayon sa LTFRB, layunin ng programang ito na gawing 
                    <span
                        class="font-bold  decoration-primary/80 "
                        >maka-bago, 
                        maka-kalikasan,
                        at ligtas
                    </span>
                    ang sistema ng transportasyon sa bansa sa pamamagitan ng:
                </p>
                <ol class="mx-3 my-2">
                    <li><strong>1)</strong> Pag-phaseout o pagtanggal sa mga maka-lumang sasakyan,</li>
                    <li><strong>2)</strong> Pag-implementa ng bagong ruta,</li>
                    <li><strong>3)</strong> Pag-engganyo sa mga indibidwal na tsuper na magsama-sama at bumuo ng kooperatiba, at </li>
                    <li><strong>4)</strong> Pagtakda ng mga bagong kwalipikasyon na kakailanganin para sa bawat dyip. </li>
                </ol>                 
                 
        
		</div>
		<div class="relative h-full">
			<img
				class="h-full w-full rounded-lg object-cover"
				src={jeep1}
				alt="#NoToJeepneyPhaseout Rally"
			/>
		</div>
	</section>
    <section
		class="w-full bg-gradient-radial from-transparent to-blue-300 dark:from-primary dark:to-transparent"
		id="problem"
	>
		<div class="mx-auto flex max-w-6xl flex-col gap-6 px-4 py-20">
			<div>
				<h1
					class="font-jeepney text-8xl font-extrabold tracking-tight text-blue-500 drop-shadow-md dark:text-green-400"
				>
					02
				</h1>
				<h1
					class="font-jeep text-7xl uppercase tracking-tight text-blue-500 drop-shadow-lg dark:text-orange-500"
				>
					Problem
				</h1>
			</div>
			<div class="flex auto-rows-auto grid-cols-4 flex-col gap-8 md:grid">
				<div
					class="col-span-4 row-span-2 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
				>
					<h2 class="scroll-m-20 pb-2 text-3xl font-bold tracking-tight">Background</h2>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						Sa unang tingin, tila magandang mungkahi ang JMP dahil pinagbubuti nito ang kapakanan ng mga pasahero at ginagawang mas organisado ang pamamahala ng dyip, gayunpaman, maraming tsuper ang tumutol sa pag-implementa nito.
Sa kadahilanan na hindi nasasaalang-alang ng pamahalaan ang kapakanan ng unang maaapektuhan ng programang ito, ang mga tsuper at operator. Imbis na makatulong, makasasagabal at mailalagay sa panganib ang kabuhayan ng mga drayber kung agarang iangkop ang JMP. 
					</p>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						Bilang pagtutol sa implementasyon ng JMP, nagsagawa ang mga tsuper ng kilos protesta sa pamamagitan ng tigil pasada/transport strike. Sa katunayan, nagsimula pa ito noong inilunsad ang programa noong 2017 at nagpapatuloy hanggang sa kasalukuyan.
					</p>
				</div>
            </div>
        </div>
	</section>
    <section class="mx-auto flex h-full max-w-6xl items-center gap-8 px-4 py-20 md:grid md:h-screen md:gap-16">
        <div>
            <h1
				class= "font-jeep text-5xl tracking-tight text-blue-500 drop-shadow-lg dark:text-orange-500">
                Tunay na epektibo ang mga nagdaang tigil-pasada dahil ...
            </h1>
            <h2> sample </h2>
            <p>dslhfidh</p>
        </div>
    </section>

</main>