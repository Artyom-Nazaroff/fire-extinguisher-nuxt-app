<template>
		<div class="container">
			<LargeCardDisplay
				v-for="cardInfo in largeCardInfo.slice(0,1)"
				:key="cardInfo.id"
				:cardsSection="cardInfo"
			/>
			<SmallCardDisplay
				v-for="cardInfo in smallCardInfo"
				:key="cardInfo.id"
				:cardsSection="cardInfo"
			/>
		</div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data';

export default {
	data: () => ({
		largeCardInfo: largeCardSections,
		smallCardInfo: smallCardSections,
	})
}
</script>

<style>

</style>