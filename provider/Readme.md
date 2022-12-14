# BlockWallet Provider's Remote Configuration
This package includes all the configurations related to BlockWallet's provider. Be aware that every change included here will directly impact the production environment.

### Incompatible sites
The incompatible sites list is a way to determine which DApp BlockWallet's extension is compatible. To add new sites, please update the `incompatible_sites.json` by adding/removing lines using the JSON format. 

#### How to include a new site?
DApps may have different applications (staking, swaps, trading, and so on) divided by subdomains making their URL to change depending on the product you are using. For example: 

Let's think about a DApp whose main page is `incompatibledapp.io` and their swaps and staking products are allocated in `swap.incompatibledapp.io` and `staking.incompatibledapp.io` respectively, and you want to add it to the `incompatible_sites.json` file. 
You can: 
1. Add the URL, including the subdomains forcing you to add two new lines to the file: `swap.incompatibledapp.io` and `staking.incompatibledapp.io`.
2. **[Recommended]** Add only one line by removing the subdomain: `incompatibledapp.io`. By doing this, you will handle every new subdomain/product added to the DApp.

You can check an example here: https://github.com/block-wallet/remote-configs/pull/4

