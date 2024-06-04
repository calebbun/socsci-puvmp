<script global>
    import '../global.css'
    import jeep1 from '$lib/assets/jeep1.jpg';
	import jeepmove from '$lib/assets/jeepmove.png';
	import wheel from '$lib/assets/wheel.png';
	import sun from '$lib/assets/sun.png';
	import sun2 from '$lib/assets/sun2.png';
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
	*
	{
		box-sizing: border-box;
	}
	.road{
		position: relative;
		width: 100vw;
		display: flex;
		justify-content: center;
		align-items: center;
		transform-style: preserve-3d;
	}

	.road::before{
		content: '';
		position: absolute;
		width: 100%;
		height: 4px;
		background: linear-gradient(90deg, #fff, #fff 50%, transparent 50%, transparent 100%);
		background-size: 50px;
		animation: animate_road 1s linear infinite;
		z-index: -1;
	}	

	.jeep{
		animation: animate_jeep 9s linear infinite;
		z-index: 1;
	}

	@keyframes animate_road
	{
		0%{
			background-position: 50px 0;
		}
		100%{
			background-position: 0px 0;
		}
	}
	@keyframes animate_jeep {
		0% {
			transform: translateX(-1100%) translateY(0);
		}
		25% {
			transform: translateX(-233%) translateY(30%);
		}
		50% {
			transform: translateX(0%) translateY(0);
		}
		75% {
			transform: translateX(233%) translateY(-30%);
		}
		100% {
			transform: translateX(1100%) translateY(0);
		}
		
	}

	
</style>
<head>
	<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
	<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
	<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
	<link rel="manifest" href="/site.webmanifest">
	<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#5bbad5">
	<meta name="msapplication-TileColor" content="#da532c">
	<meta name="theme-color" content="#ffffff">
</head>

<main>
    <section
    class="relative w-full h-[screen/3]"
	>
        <video class= "absolute w-full h-full object-cover -z-10"muted autoplay loop playsinline disablepictureinpicture>
            <source src="baguiodrive.mp4" type="video/mp4" />
        </video>
            
        <div
			class="shadowed-text min-h-screen-minus-navbar mx-auto flex max-w-6xl flex-col items-center justify-center gap-2 py-16 pt-12 text-center pb-0"
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
	<section>
		<div class="relative overflow-hidden h-[6vh] flex justify-center items-center bg-[#355463]">
			<div class="absolute h-[3vh] w-[10vh] jeep ">
				<img src={jeepmove} alt="jeep design side view"> 
			</div>
			<div class="road"></div>
		</div>
	</section>
    <section
		class="relative mt-0 pt-8 mx-auto flex h-screen flex-col items-center justify-center gap-2 py-20 text-center">
	
		<div
			class="absolute z-10 h-screen-minus-navbar w-full bg-jeep2 bg-cover bg-center opacity-30 blur-sm">
			<div></div>
		</div>

		<p
			class="text-justify z-20 mx-16 max-w-[850px] text-2xl font-medium leading-tight hover:drop-shadow-2xl md:text-3xl [&:not(:first-child)]:mt-6"
		>
        Noong 2014 naglabas ng pag-aaral ang Japan International Cooperation Agency (JICA) na napag-alamang nakakaltasan tayo ng P2.4 bilyon kada araw dahil sa trapiko. Bilang pagtugon sa suliraning ito, noong June 19, 2017, naglabas ng bagong programa ang Department of Transportation o DOTr na naglalayong pagandahin at gawing mas moderno ang mga pampublikong sasakyan at agapan ang lumalaking problema sa trapik. Ang programang ito’y mas kilala bilang Jeepney Modernization Program (JMP) na sumasailalim sa  

			<span
				class="font-bold underline decoration-primary/80 decoration-4 duration-200 ease-in hover:text-primary hover:decoration-transparent"
				>Public Utility Vehicle  Modernization Program o PUVMP.
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
                    PUVMP
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
					HINAING
				</h1>
			</div>
			<div class="flex auto-rows-auto grid-cols-4 flex-col gap-8 md:grid">
				<div
					class="col-span-4 row-span-2 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
				>
					<!-- <h2 class="scroll-m-20 pb-2 text-3xl font-bold tracking-tight"></h2> -->
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
	<div class="bg-gradient-radial-bottom from-transparent to-orange-400">
		<section class="pb-10 mb-[1px] mx-auto flex min-h-full max-w-6xl items-center gap-8 px-4 py-20 md:grid md:min-h-screen md:gap-16">
			<div class="p-2 flex flex-col gap-2">
				<h1
					class="font-jeepney text-8xl font-extrabold tracking-tight text-white drop-shadow-md dark:text-green-400"
				>
					03
				</h1>
				<h1
					class= "text-4xl tracking-tight text-white drop-shadow-lg dark:text-orange-500">
					Tunay na epektibo ang mga nagdaang tigil-pasada dahil ...
				</h1>
				<div class="flex flex-col p-5 bg-secondary rounded-lg gap-4">
					<p class="text-lg">Maraming naging makabuluhang epekto ang mga naisagawang tigil pasada/ transport strike sa pampublikong diskurso pati na rin sa pagsasaayos at pagrebisa ng mga polisiya ng programang JMP. Isa na rito ay ang pagbibigay ng palugit sa mga tsuper para sa konsolidasyon ng prangkisa o franchise consolidation, isa sa mga pangunahing hakbang upang maisakatuparan ang programang JMP. Sa tulong ng mga tigil pasada/ transport strike ay naihayag ng mga tsuper ang kanilang hinaing ukol sa napakamahal na presyo ng isang modern jeepney unit na nagkakahalagang humigit-kumulang Php2.8 milyon, at ng mga dagdag na bayarin na kailangan upang makasali sa isang kooperatiba. Mula nang idineklara ang JMP noong 2017 ay nagkaroon na ng walong (8) beses na extension upang makasunod ang mga tsuper sa franchise consolidation at upang mabigyan ng dagdag oras ang gobyerno na higit na masuri ang mga kasalukuyang alituntunin ng JMP.
					</p>
					<p class="text-lg">
						Dinagdagan din ng Department of Transportation (DOTr) ang ibibigay na equity subsidy para sa mga tsuper at operators na bahagi ng isang kooperatiba upang magsilbing loan sa pagbili ng bagong modelong jeepney. Mula sa Php80,000 para sa isang modern PUV (mPUV) classes 1-4 noong 2018 ay itinaas na sa Php210,000 para sa class 1 at Php280,000 para sa classes 2-4 noong 2023 ang subsidiyang inaalok bilang suporta sa mga tsuper at operators sa nakikilahok sa PUVMP.
					</p>
					<p class="text-lg">
						Isa sa mga pangunahin at pinakamatagal na hinaing ng mga tsuper ay ang hindi abot-kayang presyo ng bagong modelong jeepney. Kung kaya’t nagdisenyo ang mga local manufacturers tulad ng Francisco Motors ng bagong modelo ng jeepney na higit na mas mura sa presyong Php985,000 kumpara sa idineklarang Php2.8 milyon na presyo ng mga imported modern jeepney units. Ang mga lokal na bagong modelong jeepney na ito ay kahawig ng itsura ng mga tradisyonal na dyip, maka-kalikasan dahil gumagamit ito ng elektrisidad, komportable dahil may aircon, mayroon ding daanan para sa mga pasaherong naka-wheelchair. Bukod pa rito ay Php50,000 lang ang kinakailangang downpayment na may 0% interes na higit na makakatulong sa mga tsuper at operator na namomoblema sa pambayad.
					</p>
					<p class="text-lg">
						Bilang konklusyon, makikita na ang tigil pasada/ transport strikes ay epektibong paraan upang makarating ang hinaing ng mga tsuper at operator sa mga tagagawa ng polisiya. Ilan lamang sa mga naging mabuting resulta nito ay ang pag-extend ng franchise consolidation deadline, pagtaas ng ibibigay na equity subsidy, at pagkakaroon ng lokal at mas murang bagong modelong jeepney. 
					</p>
					<p class="text-lg">
						Bilang isang indibidwal ay maaari rin tayong makilahok sa mga ito at makiisa sa panawagan ng mga tsuper. Kung abala nama’y maaari ring mag-donate sa mga transport groups tuwing nagsasagawa ng strike dahil inaalay nila ang kanilang kita upang ipaalam ang kanilang mga hinaing. Maaari mo ring gamitin ang #NoToJeepneyPhaseout sa social media upang mapalakas ang tinig ng mga tsuper. Makapangyarihan ang boses nating mga indibidwal, kaya gamitin natin ito upang tulungan ang mga tsuper na naghihirap dahil sa PUVMP.
					</p>
					
				</div>
			</div>
		</section>


		<section class="mx-auto flex h-full max-w-6xl items-center gap-8 px-4 pb-6">
			<div class="w-[40vh] flex flex-shrink-0 justify-center align-center">
				<img src={wheel} alt="cartoon wheel spinning" class="w-3/4 animate-spin-slow"> 
			</div>
			<div class="flex-grow h-[100%] w-[80%]">
				<div class="p-4 bg-secondary rounded-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl flex flex-col gap-2">
					<p class="text-lg">Madalas nating marinig na</p>
					<p class="text-3xl text-blue-600"><strong>“Ang buhay ay parang gulong minsan nasa taas minsan nasa baba.”</strong></p>
					<p class="text-lg">Ngunit tila laging nasa ibaba ang mga tsuper dahil sa di makatarungang pag-implementa ng Jeepney Modernization Program. Parte sila ng byahe, <u>sila ang tagapagmaneho ng byaheng patungo sa inaasam nating modernisasyon.</u></p>
				</div>
			</div>
		</section>
		<footer style="position:relative">
			<div class="pt-3">
				<p class="text-center text-2xl">Suportahan ang ating mga tsuper sa pamamagitan ng:</p>
			</div>
			<div class="flex justify-center items-center gap-10 mb-20">
				<a target="_blank" href="https://www.facebook.com/pistonphl" class="text-2xl hover:underline text-blue-700">FOLLOW PISTON'S FB PAGE</a>
				<a target="_blank" href="https://donate.pistonph.com" class="text-2xl text-blue-700 hover:underline">DONATE TO PISTON</a>
			</div>
			<div class="w-[22vh] flex flex-shrink-0 justify-center align-center" style="position: absolute; bottom: 10%; left: 50vw; transform: translateX(-50%)">
				<img src={sun2} alt="cartoon sun spinning" class="z-0 w-3/4 animate-spin-slower"> 
			</div>
			<div class="z-10" style="position: relative;">
				<p class=" bg-blue-700 text-center text-xl text-white">#LabanNgTsuperLabanNgKomyuter #NoToJeepneyPhaseout</p>
			</div>
			<div class="relative overflow-hidden min-h-[6vh] flex justify-center items-center bg-[#355463]">
				<div class="absolute h-[3vh] w-[10vh] jeep ">
					<img src={jeepmove} alt="jeep design side view"> 
				</div>
				<div class="road"></div>
			</div>
		</footer>
	</div>
</main>