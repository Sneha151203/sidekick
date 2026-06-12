<div class="card">
	<h1>🔀 Workflow Editor</h1>

	<div class="workflow">
		<div class="node trigger">
			📥 Trigger
		</div>

		<div class="connector">↓</div>

		<div class="node process">
			⚙️ Process Data
		</div>

		<div class="connector">↓</div>

		<div class="node ai">
			🤖 AI Agent
		</div>

		<div class="connector">↓</div>

		<div class="node output">
			📤 Output
		</div>
	</div>
</div>

<style>
	.card {
		background: white;
		padding: 25px;
		border-radius: 16px;
		border: 3px solid #2563eb;
		box-shadow: 0 10px 25px rgba(0,0,0,0.15);
	}

	.workflow {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-top: 30px;
	}

	.node {
		width: 220px;
		padding: 15px;
		border-radius: 12px;
		text-align: center;
		font-weight: bold;
		color: white;
		margin: 5px 0;
	}

	.trigger {
		background: #16a34a;
	}

	.process {
		background: #ea580c;
	}

	.ai {
		background: #7c3aed;
	}

	.output {
		background: #2563eb;
	}

	.connector {
		font-size: 28px;
		font-weight: bold;
		margin: 5px 0;
	}
</style>