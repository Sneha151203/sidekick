<div class="card">
	<h1>🎲 3D Animation</h1>

	<div class="animation-box">
		<div class="cube">🚀</div>
	</div>

	<p>
		This section will contain the Threlte 3D animation.
	</p>
</div>

<style>
	.card {
		background: white;
		padding: 25px;
		border-radius: 12px;
		border: 3px solid #2563eb;
		box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
	}

	.animation-box {
		height: 250px;
		display: flex;
		align-items: center;
		justify-content: center;
		margin: 20px 0;
		border: 2px dashed #2563eb;
		border-radius: 12px;
	}

	.cube {
		font-size: 80px;
		animation: spin 4s linear infinite;
	}

	@keyframes spin {
		from {
			transform: rotate(0deg);
		}
		to {
			transform: rotate(360deg);
		}
	}
</style>