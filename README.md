# Metahash Rewards
Metahash Rewards is a automated PHP script to pay bonus rewards to delegators from [MetaHash](https://metahash.org ) nodes.

### Requirements

- PHP 7.1+
- ext-gmp
- ext-curl
- composer
- xboston/metahash-php 0.2.2

### Installation

1. Download master.zip or clone repository and unpackage to your chosen folder.

2. Open your terminal and change directory to where you unpackaged metahash-rewards.

```bash
cd path/to/your/folder/metahash-rewards/
```

3. Run the following command in your terminal.

```bash
composer install
```

4. Open the index.php and enter your node details in the $nodes array.

```php
$nodes = [
  'address'         => '', // Node address.
  'private_key'     => '', // Node private Key.
  'data'            => '', // Data sent with transaction.
  'percentage'      => 80, // Default percentage paid to delegators.
  'superAddresses'  => $superAddresses
];
```

Please note: when index.php is opened in your browser, the script will run... if testing, comment out line 35 in index,php to stop payments being sent. here is an example:
```php
if(!isset($payees['error'])) :
  // $results = $node->sendPayments($payees, $nodes);
endif;
```
