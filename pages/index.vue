<template>
		<div class="container">
			<Hero/>
			<LargeCardDisplay
				v-for="cardInfo in largeCardInfo"
				:key="cardInfo.id"
				:cardsSection="cardInfo"
			/>
			<SmallCardDisplay
				v-for="cardInfo in smallCardSections"
				:key="cardInfo.id"
				:cardsSection="cardInfo"
			/>
		</div>
</template>

<script>
import { largeCardSections, smallCardSections } from '~/assets/data';

export default {
	data: () => ({
		largeCardInfo: largeCardSections,
		smallCardSections,
	})
}
</script>
