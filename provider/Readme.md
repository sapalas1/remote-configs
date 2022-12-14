# BlockWallet Provider's Remote Configuration
This package includes all the configuration related to the BlockWallet's porvider.  Be aware that every change included here will have direct impact to the production environment.

### Incompatible sites
The incompatible sites list is a way to know to which DApp the BlockWallet's extension is compatible. In order to add new sites, please update the `incompatible_sites.json` by adding/removing lines using the JSON format. 

#### How to include a new site?
DApp's may have different applications (staking, swaps, trading, so on) divided by subdomains making their url to split depending on the production you are using. For example: 

Lets think about a DApp which main page is `incompatibledapp.io` and their swaps and staking products are allocated in `swap.incompatibledapp.io` and `staking.incompatibledapp.io` respectively and you want to add it to the `incompatible_sites.json` file. 
You can: 
1. Add the URL including the subdomains forcing you to add 2 new lines to the file: `swap.incompatibledapp.io` and `staking.incompatibledapp.io`.
2. Add only one line by removing the subdomain: `incompatibledapp.io`. By doing this, you will handle every new subdomain/product added to the DApp.
