<template>
	<ion-page class="video-bg h-100 ion-justify-content-center ion-align-items-center">
		<div class="stars">

		</div>
		<div class="text-dark ion-padding ion-margin">
			<b>SAC</b> - The Secure Anonymous Chat
		</div>
		<a href="#" class="neon-button">Start</a>
	</ion-page>
</template>
<script lang="ts">
	import { defineComponent } from 'vue';
	import { IonButtons, IonContent, IonHeader, IonMenuButton, IonPage, IonButton, IonTitle, IonToolbar } from '@ionic/vue';

	export default defineComponent({
		name: 'HomePage',
		components: {
			/*IonButtons,
			IonContent,
			IonHeader,
			IonMenuButton,*/
			IonPage,
			//IonTitle,
			//IonToolbar
			// IonButton
		}
	});
</script>
<style lang="css">
	.video-bg {

	}

	.neon-button {
		font-size: 4em;

		display: inline-block;
		cursor: pointer;
		text-decoration: none;
		color: var(--ion-color-custom);
		border: var(--ion-color-custom) 0.125em solid;
		padding: 0.25em 1em;
		border-radius: 0.25em;

		text-shadow:
			0 0 0.125em hsl(0 0% 100% / 0.3),
			0 0 0.45em var(--ion-color-custom);

		box-shadow: inset 0 0 0.5em 0 var(--ion-color-custom), 0 0 0.5em 0 var(--ion-color-custom);
		position: relative;

	}

	.neon-button::before {
		pointer-events: none;
		content: '';
		position: absolute;
		background: var(--ion-color-custom);
		top: 120%;
		left: 0;
		width: 100%;
		height: 100%;

		transform: perspective(1em) rotateX(40deg) scale(1, 0.35);
		filter: blur(1em);
		opacity: 0.7;
		transition: filter 100ms linear;
	}

	.neon-button::after {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		bottom: 0;
		right: 0;
		box-shadow: 0 0 2em 0.5em var(--ion-color-custom);
		opacity: 0;
		background-color: var(--ion-color-custom);
		z-index: -1;
		transition: opacity 100ms linear;
	}

	.neon-button:hover,
	.neon-button:focus {
		color: var(--ion-text-color);
		text-shadow: none;
	}

	.neon-button:hover::before,
	.neon-button:focus::before {
		opacity: 1;
		filter: blur(2em);
	}

	.neon-button:hover::after,
	.neon-button:focus::after {
		opacity: 1;
	}
</style>