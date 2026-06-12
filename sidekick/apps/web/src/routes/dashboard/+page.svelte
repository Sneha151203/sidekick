<script lang="ts">
	import ResumeTab from '$lib/components/ResumeTab.svelte';
	import AnimationTab from '$lib/components/AnimationTab.svelte';
	import WorkflowTab from '$lib/components/WorkflowTab.svelte';

	let activeTab = $state('resume');
</script>

<div class="dashboard">
	<aside class="sidebar">
		<h2>SideKick</h2>

		<button onclick={() => activeTab = 'resume'}>
			📄 Resume
		</button>

		<button onclick={() => activeTab = 'animation'}>
			🎲 Animation
		</button>

		<button onclick={() => activeTab = 'workflow'}>
			🔀 Workflow
		</button>
	</aside>

	<main class="content">
		{#if activeTab === 'resume'}
			<ResumeTab />
		{/if}

		{#if activeTab === 'animation'}
			<AnimationTab />
		{/if}

		{#if activeTab === 'workflow'}
			<WorkflowTab />
		{/if}
	</main>
</div>

<style>
	.dashboard {
		display: flex;
		height: 100vh;
		font-family: Arial, sans-serif;
	}

	.sidebar {
		width: 250px;
		background: #1e293b;
		color: white;
		padding: 20px;
		display: flex;
		flex-direction: column;
		gap: 10px;
	}

	.sidebar button {
		padding: 12px;
		border: none;
		border-radius: 8px;
		cursor: pointer;
		font-size: 16px;
	}

	.content {
		flex: 1;
		padding: 30px;
		background: #f8fafc;
	}
</style>