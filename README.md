# Run promotions and discounts for Black Friday and Cyber Monday

Black Friday and Cyber Monday discounts offer special deals during promotions to attract new customers and boost sales. They are limited-time discounts, typically valid for a short period, and can apply to specific products or all items in your catalog. Paddle offers several options to fully customize discounts on your products.

To start:

**Log in** to Paddle Dashboard
Start by logging into your Paddle Dashboard. If you do not have a Paddle account, [sign up](https://login.paddle.com/signup "sign up") and complete the initial setup.

**Navigate** to Discounts
In the Paddle Dashboard, navigate to the **Discounts** section under the **Catalog** option.

#### Create a New Discount
To create a new discount, select **+ New Discount**

Select the **discount type**.

There are three discount type options available: 

- Percentage: Fill out the percentage off details.
- Amount: Fill out the amount details and select the currency.
- Amount per unit: Fill out the amount details and select the currency.   Enter a descriptive name for the discount for example, 'Black Friday Sale'.

Black Friday - Cyber Monday discounts can be either **one time discounts** or **recurring discounts**. 

To create a one time Black friday - Cyber Monday Discount, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#create-a-one-time-discount "guide") on how to create a one time discount.

To create a recurring Black friday - Cyber Monday Discount, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#create-a-recurring-discount "guide") on how to create a recurring discount.

#### Usage and expiry limits on Discount and Promotions

Since Black Friday - Cyber Monday discounts are time limited discounts as they last for only the duration of this period, you will need to set a limit on discounts offered within this period.

To set a time limit to discounts created within Black Friday - Cyber Monday, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#create-a-limited-time-discount "guide")

#### Checkout discount code 

Set the **Checkout discount code** toggle on.
Set a discount code or select the **Generate random code** option.

#### Add discounts to selected products

If you would like to add discounts to only selected products within your catalog, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#limit-discounts-to-certain-products "guide")

When you are done you should select the **create** button, this creates a new discount.

#### Find out how many times a discount has been redeemed

You might want to check how many times the Black Friday - Cyber Monday discount has been used, this can help you keep track of how many customers purchased your product or know what products were popular during this period, you can also use this information to generate traffic to a specific product.

If you would like to find out how many times a discount has been redeemed, check this [guide](https://developer.paddle.com/build/products/offer-discounts-promotions-coupons#see-how-many-times-a-discount-has-been-redeemed "guide").

#### API REQUEST

This example creates a new Black Friday discount which:

- Takes $30 off a transaction.
- Does not recur.
- Only applies to two price IDs.
- Can't be applied by customers using a code
- Doesn't expire.
- Has no limit on the number of times it can be applied

```
{
  "description": "Nonprofit discount",
  "type": "flat",
  "amount": "1000",
  "currency_code": "USD",
  "recur": true,
  "maximum_recurring_intervals": null,
  "restrict_to": [
    "pri_01gsz8z1q1n00f12qt82y31smh",
    "pri_01gsz8s48pyr4mbhvv2xfggesg"
  ]
}
```
#### RESPONSE 

If successful, Paddle will respond with a copy of the newly created discount entity

```
{
  "data": {
    "id": "dsc_01gtf15svsqzgp9325ss4ebmwt",
    "description": "Nonprofit discount",
    "status": "active",
    "enabled_for_checkout": false,
    "code": null,
    "type": "flat",
    "amount": "1000",
    "currency_code": "USD",
    "recur": true,
    "maximum_recurring_intervals": null,
    "usage_limit": null,
    "restrict_to": [
      "pri_01gsz8z1q1n00f12qt82y31smh",
      "pri_01gsz8s48pyr4mbhvv2xfggesg"
    ],
    "expires_at": null,
    "times_used": 0,
    "created_at": "2023-03-01T16:48:04.473Z",
    "updated_at": "2023-03-02T08:31:19.035Z"
  }
}
```

