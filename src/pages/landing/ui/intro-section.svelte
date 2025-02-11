<script lang="ts">
	import MaleProgrammer from '../../../entities/svg-images/ui/male-programmer.svelte';
	import SnsBlock from '../../../widgets/SnsBlock/ui/sns-block.svelte';
</script>

<section class="intro-section">
	<div class="flex flex-col-reverse max-lg:gap-12 lg:flex-row">
		<div class="flex basis-1/2 flex-col justify-center gap-6 max-lg:items-center">
			<h2 class="text-4xl font-extrabold max-lg:text-center md:max-lg:text-5xl lg:text-6xl">
				안녕하세요 👋<br />
				프론트엔드 개발자 <br /> 유승범입니다
			</h2>
			<p class="max-lg:text-center">
				새로운 기술과 문제를 마주할 때 가장 큰 즐거움을 느낍니다. 매 순간 더 나은 방법을 고민하며,
				실패를 두려워하지 않고 도전합니다. 변화와 성장을 추구하며, 협업을 통해 더 큰 가치를
				만들어가는 개발자가 되려고 노력하고 있습니다
			</p>
		</div>
		<div class="mb-[-12px] flex basis-1/2 justify-center object-cover">
			<div class="w-full max-w-[450px]">
				<MaleProgrammer></MaleProgrammer>
			</div>
		</div>
	</div>
	<div class="flex w-full items-center">
		<div class="mobile-sns-section">
			<SnsBlock />
		</div>
		<div class="h-[2px] basis-3/4 bg-black dark:bg-white max-lg:hidden"></div>
	</div>
</section>

<style lang="postcss">
	.intro-section {
		@apply flex h-screen flex-col items-center;
	}

	.mobile-sns-section {
		@apply flex basis-1/4 max-lg:basis-full max-lg:justify-center;
	}
</style>
