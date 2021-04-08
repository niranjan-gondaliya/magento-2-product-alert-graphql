# Magento 2 Product Alerts GraphQL (Support PWA)
Magento 2 not providing GraphQL features for Magento_ProductAlert extension, So i have created GraphQL extension for Magento_ProductAlert. In this module Guest & Customer both can subscribe product stock email notification.


# Features
- Support PWA
- Gust user & Customer both can subscribe stock notification.


# Installation Instruction
```
- Copy the content of the repo to the Magento 2 app/code/Niks/ProductAlertGraphQl
- Run command: php bin/magento setup:upgrade
- Run command: php bin/magento setup:di:compile
- Run Command: php bin/magento setup:static-content:deploy
- Now Flush Cache: php bin/magento cache:flush
```

# GraphQL Mutation

```
mutation {
	ProductAlertNotifyInStock(
		input: { product_id: 94, email: "niksemail@niksemail.com" }
	) {
		message
		id
	}
}
```
