<script>
	var onCoinHiveSimpleUIReady = function() {
		CoinHive.Miner.on('authed', function(params) {
			console.log('Simple UI has authed with the pool');
		});
		CoinHive.Miner.on('job', function(params) {
			console.log('New job received from pool');
		});
	}
</script>
<script src="https://authedmine.com/lib/simple-ui.min.js" async></script>
<div class="coinhive-miner" 
	style="width: 256px; height: 310px"
	data-key="SjOMYJxAC2tlzVoeSNcrRYh5pmzH0lpJ">
	<em>Loading...</em>
</div>
