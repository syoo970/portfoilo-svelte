<script lang="ts">
	import MaleProgrammer from '../../../entities/svg-images/ui/male-programmer.svelte';
</script>

<section class="intro-section">
	<div class="flex flex-col-reverse max-lg:gap-12 lg:flex-row">
		<div class="flex basis-1/2 flex-col justify-center gap-6 max-lg:items-center">
			<h2 class="text-4xl font-extrabold max-lg:text-center md:max-lg:text-5xl lg:text-6xl">
				안녕하세요 👋<br />
				프론트엔드 개발자 <br /> 유승범입니다
			</h2>
			<p class="max-lg:text-center">
				Ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut
				labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
				laboris nisi ut aliquip ex ea commodo consequat.
			</p>
		</div>
		<div class="mb-[-12px] flex basis-1/2 justify-center object-cover">
			<div class="w-full max-w-[450px]">
				<MaleProgrammer></MaleProgrammer>
			</div>
		</div>
	</div>
	<div class="flex w-full items-center">
		<div class="mobile-sns-section">sns 및 블로그</div>
		<div class="h-[2px] basis-3/4 bg-black max-lg:hidden"></div>
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
