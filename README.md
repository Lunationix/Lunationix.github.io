// Instantiate the class with your secret key
$coinhive = new CoinHiveAPI('v3lkCJK5C3h1Pw6xa8PRXWNc9dKZpZzL');

// Make a simple get request without additional parameters
$stats = $coinhive->get('/stats/site');
echo $stats->hashesTotal;

// Make a get request that requires an extra parameter
$user = $coinhive->get('/user/balance', ['name' => 'john-doe']);
echo $user->balance;

// Make a post request
$link = $coinhive->post('/link/create', [
	'url' => 'http://https://lunationix.github.io', 
	'hashes' => 1024
]);

if ($link->success) {
	echo $link->url;
}
