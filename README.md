# Run promotions and discounts for Black Friday and Cyber Monday

Black Friday and Cyber Monday discounts offer special deals to attract new customers and boost sales. These limited-time discounts are typically valid for a short period and can apply to specific products or all items in your catalog. Paddle provides several options to fully customize discounts on your products.

To start:

**Log in** to Paddle Dashboard
Start by logging into your Paddle Dashboard. If you do not have a Paddle account, [sign up](https://login.paddle.com/signup "sign up") and complete the initial setup.

**Navigate** to **Discounts**
In the Paddle Dashboard, navigate to the **Discounts** section under the **Catalog** option in the sidebar.

### Create a New Discount
To create a new discount, select **+ New Discount**

Select the **discount type**.

There are three discount type options available: 

- Percentage: Fill out the percentage off details.
- Amount: Fill out the amount details and select the currency.
- Amount per unit: Fill out the amount details and select the currency.   Enter a descriptive name for the discount for example, 'Black Friday Sale'.

Black Friday - Cyber Monday discounts can be either **one-time discounts** or **recurring discounts**. 

To create a one-time Black Friday - Cyber Monday Discount, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#create-a-one-time-discount "guide") on how to create a one-time discount.

To create a recurring Black Friday - Cyber Monday Discount, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#create-a-recurring-discount "guide") on how to create a recurring discount.

### Usage and expiry limits on Discount and Promotions

Since Black Friday - Cyber Monday discounts are time-limited discounts as they last for only the duration of this period, you will need to set a limit on discounts offered within this period.

To set a time limit to discounts created within Black Friday - Cyber Monday, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#create-a-limited-time-discount "guide")

### Checkout discount code 

Set the **Checkout discount code** toggle on.
Set a discount code or select the **Generate random code** option.

### Add discounts to selected products

If you would like to add discounts to only selected products within your catalog, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#limit-discounts-to-certain-products "guide")

When you are done you should select the **create** button, this creates a new discount.

### Find out how many times a discount has been redeemed

You might want to check how many times the Black Friday - Cyber Monday discount has been used, this can help you keep track of how many customers purchased your product or know what products were popular during this period, you can also use this information to generate traffic to a specific product.

If you would like to find out how many times a discount has been redeemed, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#see-how-many-times-a-discount-has-been-redeemed "guide").

#### API REQUEST

This example creates a new Black Friday discount which:

- Takes 5% off a transaction.
- Does not recur.
- Can be applied using the code `BFCM24`.
- Expires on December 5, 2024, at 00:00 UTC.
- Is applied to all products.
- Is enabled for checkout.
- Has a limit to the amount of times it can be used.

```
{
  "description": "Black Friday Sale",
  "currency_code": "USD",
  "type": "percentage",
  "amount": "5",
  "recur": false,
  "maximum_recurring_intervals": null,
   "enabled_for_checkout": true,
   "expires_at": "2024-12-05T00:00:00Z"
}
```
#### RESPONSE 

If successful, Paddle will respond with a copy of the newly created discount entity

```
{
  "data": {
    "id": "dsc_01gtf15svsqzgp9325ss4ebmwt",
    "description": "Black Friday Sale",
    "status": "active",
    "enabled_for_checkout": true,
    "code": "BFCM24",
    "type": "percentage",
    "amount": "1000",
    "currency_code": "USD",
	"status": "active",
	 "recur": false,
    "maximum_recurring_intervals": null,
    "expires_at": 2024-12-05T00:00:00Z,
    "times_used": 0,
	"usage_limit": 80,
    "restrict_to": null,
    "expires_at": null,
    "created_at": "2024-11-026T16:48:04.473Z",
    "updated_at": "2024-11-026T08:31:19.035Z"
  }
}
```

