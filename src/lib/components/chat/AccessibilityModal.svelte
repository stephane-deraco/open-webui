<script lang="ts">
	import { getContext } from 'svelte';
	import Modal from '../common/Modal.svelte';

	const i18n = getContext('i18n');

	export let show = false;
</script>

<Modal bind:show>
	<div class="text-gray-700 dark:text-gray-100">
		<div class=" flex justify-between dark:text-gray-300 px-5 pt-4">
			<div class=" text-lg font-medium self-center">{$i18n.t('Accessibility: not compliant.')}</div>
			<button
				class="self-center"
				on:click={() => {
					show = false;
				}}
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 20 20"
					fill="currentColor"
					class="w-5 h-5"
				>
					<path
						d="M6.28 5.22a.75.75 0 00-1.06 1.06L8.94 10l-3.72 3.72a.75.75 0 101.06 1.06L10 11.06l3.72 3.72a.75.75 0 101.06-1.06L11.06 10l3.72-3.72a.75.75 0 00-1.06-1.06L10 8.94 6.28 5.22z"
					/>
				</svg>
			</button>
		</div>

		<div class="flex flex-col md:flex-row w-full p-5 md:space-x-4 dark:text-gray-200">

            <h1>Déclaration d'accessibilité</h1>
            <p>Le CNRS s’engage à rendre ses sites accessibles conformément à l’article 47 de la loi n° 2005-102 du 11 février
              2005. À cette fin, il met en œuvre la stratégie et les actions au travers du schéma pluriannuel et du plan d'action
              annuel qui sont en cours d'élaboration. <br>
              Cette déclaration d’accessibilité s’applique à [nom du service/site].</p>
            <h2>État de conformité </h2>
            <p>[nom du service/site] est non conforme au référentiel général d’amélioration de l’accessibilité, RGAA version 4.1.
            </p>
            <h2>Résultats des tests</h2>
            <p>L’audit de conformité n'a pas encore été réalisé pour révéler le niveau de conformité.</p>
            <h2>Contenus non accessibles</h2>
            <p>Les contenus non accessibles seront listés ci-dessous avec les raisons une fois l'audit effectué.</p>
            <h2>Établissement de cette déclaration d’accessibilité</h2>
            <p>Cette déclaration a été établie le [JJ mois AAAA]. [Elle a été mise à jour le [JJ mois AAAA]].</p>
            <h2>Retour d’information et contact </h2>
            <p> Si vous n’arrivez pas à accéder à un contenu ou à un service, vous pouvez contacter le référent accessibilité du
              CNRS pour être orienté vers une alternative accessible ou obtenir le contenu sous une autre forme.<br>
              Contacter <a href="mailto:referent-accessibilite@cnrs.fr">referent-accessibilite@cnrs.fr</a> (mail en attente de
              confirmation) </p>
            <h2>Voies de recours </h2>
            <p>Cette procédure est à utiliser dans le cas suivant.<br>Vous avez signalé au référent accessibilité du CNRS un
              défaut d’accessibilité qui vous empêche d’accéder à un contenu ou à un service et vous n’avez pas obtenu de réponse
              satisfaisante.<br>
			</p>
            <ul>
              <li>Écrire un message au Défenseur des droits :<br>
                <a href="https://formulaire.defenseurdesdroits.fr/formulaire_saisine/"
                  target="_blank">https://formulaire.defenseurdesdroits.fr/formulaire_saisine</a>
              </li>
              <li>Contacter le délégué du Défenseur des droits dans votre région :<br>
                <a href="https://www.defenseurdesdroits.fr/carte-des-delegues/"
                  target="_blank">https://www.defenseurdesdroits.fr/carte-des-delegues</a>
              </li>
              <li>Envoyer un courrier par la poste (gratuit, ne pas mettre de timbre) <br>
                Défenseur des droits <br>
                Libre réponse 71120 <br>
                75342 Paris CEDEX 07</li>
            </ul>
            



		</div>


	</div>
</Modal>

<style>
	input::-webkit-outer-spin-button,
	input::-webkit-inner-spin-button {
		/* display: none; <- Crashes Chrome on hover */
		-webkit-appearance: none;
		margin: 0; /* <-- Apparently some margin are still there even though it's hidden */
	}

	.tabs::-webkit-scrollbar {
		display: none; /* for Chrome, Safari and Opera */
	}

	.tabs {
		-ms-overflow-style: none; /* IE and Edge */
		scrollbar-width: none; /* Firefox */
	}

	input[type='number'] {
		-moz-appearance: textfield; /* Firefox */
	}
</style>
