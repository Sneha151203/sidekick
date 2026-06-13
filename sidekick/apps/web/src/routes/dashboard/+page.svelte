<script lang="ts">
	import ResumeTab from '$lib/components/ResumeTab.svelte';
	import AnimationTab from '$lib/components/AnimationTab.svelte';
	import WorkflowTab from '$lib/components/WorkflowTab.svelte';

	let activeTab = $state('resume');
</script>

<div class="dashboard">
	<h1>🚀 SideKick Dashboard</h1>

	<div class="tabs">
		<button
			class:active={activeTab === 'resume'}
			onclick={() => (activeTab = 'resume')}
		>
			Resume
		</button>

		<button
			class:active={activeTab === 'animation'}
			onclick={() => (activeTab = 'animation')}
		>
			Animation
		</button>

		<button
			class:active={activeTab === 'workflow'}
			onclick={() => (activeTab = 'workflow')}
		>
			Workflow
		</button>
	</div>

	<div class="content">
		{#if activeTab === 'resume'}
			<ResumeTab />
		{:else if activeTab === 'animation'}
			<AnimationTab />
		{:else if activeTab === 'workflow'}
			<WorkflowTab />
		{/if}
	</div>
</div>

<style>
	.dashboard {
		max-width: 1200px;
		margin: 40px auto;
		padding: 30px;
		font-family: Arial, sans-serif;
		background: #f8fafc;
		border-radius: 20px;
		box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
	}

	h1 {
		text-align: center;
		color: #2563eb;
		margin-bottom: 30px;
		font-size: 2.5rem;
	}

	.tabs {
		display: flex;
		justify-content: center;
		gap: 15px;
		margin-bottom: 30px;
	}

	button {
		padding: 14px 28px;
		border: none;
		border-radius: 12px;
		cursor: pointer;
		font-size: 16px;
		font-weight: bold;
		background: white;
		box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
		transition: all 0.3s ease;
	}

	button:hover {
		transform: translateY(-2px);
	}

	button.active {
		background: #2563eb;
		color: white;
	}

	.content {
		display: flex;
		justify-content: center;
		margin-top: 20px;
	}
</style>