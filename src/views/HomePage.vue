<template>
	<ion-page class="video-bg h-100 ion-justify-content-center ion-align-items-center">
		<video playsinline loop poster="https://node.gameplace.space/files/thimb-1.png">
			<source src="https://node.gameplace.space/files/bg-1.mp4" type="video/mp4">
			Your browser does not support the video tag.
		</video>
		<div class="text-dark ion-padding ion-margin" style="z-index: 1">
			<b>SAC</b> - The Secure Anonymous Chat
		</div>
		<ion-button color="success" fill="outline" class="rounded">Start</ion-button>
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
			IonButton
		}
	});
</script>
<style lang="css">
	ion-button.rounded {
		border-radius: 8px!important;
	}

	video {
		object-fit: cover;
		position: absolute;
		top: 0;
		left: 0;
		height: 100%;
		width: 100%;
	}

	.video-wrapper {
		border: 2px solid #000;
		width: 300px;
		height: 300px;
		position: relative;
		overflow: hidden;
		text-align: center;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.video-bg {
		background-image: url(https://web.telegram.org/stream/%7B%22dcId%22%3A2%2C%22location%22%3A%7B%22_%22%3A%22inputDocumentFileLocation%22%2C%22id%22%3A%225330040721980268146%22%2C%22access_hash%22%3A%227434288464623762757%22%2C%22file_reference%22%3A%5B2%2C79%2C0%2C21%2C202%2C0%2C0%2C0%2C228%2C98%2C196%2C233%2C133%2C229%2C40%2C22%2C196%2C168%2C48%2C9%2C238%2C176%2C218%2C74%2C49%2C77%2C221%2C147%2C217%5D%7D%2C%22size%22%3A7619001%2C%22mimeType%22%3A%22video%2Fmp4%22%2C%22fileName%22%3A%22clouds_1.mp4%22%7D);
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