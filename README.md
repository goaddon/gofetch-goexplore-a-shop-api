# gofetch-goexplore-a-shop-api

This repository enables you to submit requests to the [Shop API](https://goaddon.com/en/addons/5b9ff6463ab42f43522b30cf?tab=shop-api) of [Gofetch](https://goaddon.com/en/addons/5b9ff6463ab42f43522b30cf) from websites hosted by [Goexplore](https://goaddon.com/en/addons/5bb227d283c3360abe01e036)'s A framework.

This repository lets you submit requests to **POST /shop_api_requests** with a payload that gets forwarded to the Gofetch Shop API. This endpoint will by default only accept requests from superusers with level 1 access.

You can allow superusers without level 1 access by assigning them permissions to the specific ecommerce platform. The easiest way to manage superuser access is through the [gofetch-goexplore-a-superuser-tools](https://github.com/goaddon/gofetch-goexplore-a-superuser-tools) repository.

You can also allow regular users who belong to the same account as the company of the webshop they are trying to interact with, by adding a `user_shop_api_endpoints` key in your Goexplore secrets. you can allow all by assigning it with the value `*`, or you can allow them individually by providing a list like this: `orders__close,variants__change_stock`.

Only superusers will be able to include the `unfiltered_response` key in requests.