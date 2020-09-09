# Maker SaaS Guide
The goal of the repository is to outline the best products and practices to use when building SaaS products. The target demographic is makers who are building one or more bootstrapped SaaS products for the web. This is a work in progress based on the experiences of real makers. The content is meant to act as a template/handbook on how to launch a SaaS product from both a technical and operational standpoint. It will cover topics like technical stack, hosting, email providers, payment providers, customer service solutions, terms of service generation, etc.

## Criteria
It is important to be intentional about your decisions when launching a SaaS product. You want to think ahead about what your goals are and use those to steer your decisions. You need to be efficient and conscious in order to make sure you are always working towards those goals.

_The goal of this guide is to help you create a profitable, low operational product while not comprising on the security of your users' data._

Everything that is recommended in this guide is taking into account that goal based on 3 core criteria that, in my opinion, should be your most important things to optimize when building your SaaS product:
  1. Price - The guide will look for solutions that are affordable. When launching a SaaS product it is important to keep the burn low so this guide will try to keep the initial spend under $50/month.
  2. Ease of integration and management - When thinking about launching a product I think about having the least time to integrate and how much time it will take to manage after the launch. This guide will optimize for both while not losing out on performance and/or reliability.
  3. Security and data privacy - This is a category that a lot sadly dismiss but this guide will focus on it. While the price is important we do not want our users' data to be sold or have the risk of being leaked so using services that care about data compliance and security is important.

## Sections
 - [Frameworks](#framworks)
 - [Hosting](#hosting)
 - [Databases](#databases)
 - [Payments](#payments)
 - [Email](#email)
 - [Terms of Service and Privacy Policy](#terms-of-service-and-privacy-policy)

#### Coding Frameworks
WIP...

#### Hosting
WIP...

#### Databases
WIP...

### Payments
Payments are one of the easier sections because there is a clear winner; [Stripe](https://stripe.com). Stripe is a perfect solution for accepting payments. With Stripe you can accept all major credit cards, ACH (bank transfers), and many other international payment types. You can set up an account for free without an incorporation. They've integrated services like [Stripe Billing](https://stripe.com/billing) to managing your reoccurring transactions, [Stripe Connect](https://stripe.com/connect) to manage payouts to customers (mainly used for marketplaces) and [Stripe Checkout](https://stripe.com/docs/payments/checkout) to help your customers enter/update their payment details without you having to build any UI.

#### Breaking it down by criteria:
- **[Pricing](https://stripe.com/pricing)**: Stripe is free to set up and you only pay a portion of each transaction. Credit card payments are `2.9% + C$0.30` and ACH payments are `$0.80% (up to $5)`.
- **Ease of integration and management**: Stripe has built one of the most well known [APIs](https://stripe.com/docs/api). It is extremely easy to set up and use. The integration using the Stripe Checkout experience with Stipe billing can be done in a few hours. This makes Stripe the ultimate solution for quick setup and easy management.
- **Security and data privacy**: Stripe has a clear [privacy policy](https://stripe.com/privacy) that outlines the data they store and how they store it.
- **Extras**: Stripe has built [Radar](https://stripe.com/radar) which is a fraud detection system that will check attributes of each transaction and spit out a score based on how likely it is to be a fraudulent payment. You can set up rules to auto decline and review payments that may be risky. It costs $0.02/transaction and it very worth it, especially when your transaction volume gets high. Another awesome part of Stripe is [Atlas](https://stripe.com/atlas) which is a program to turn your project into a company. They will set up your legal entity, and the company structure. This is a great product to simplify the process of moving from a project to a company.

#### Alternative solutions:
- **[Braintree](https://www.braintreepayments.com)** - Braintree is a competitor to Stripe, it is a PayPal company and has a lot of similar functionality. Braintree has a few unique features that Stripe does not because since it is a PayPal company. First, you can accept payments via Venmo which is a huge plus in the US since so many people us it. Plus you can use PayPal checkout which many people already use and are familiar with. This allows users to log in to their existing PayPal account so they don't have to enter their payment details on your site.
- **[Plaid](https://plaid.com/)** - Plaid is an incredible product, if you've ever connected your bank to another product you've probably used it. Plaid has built relationships with many banks in the United States and allows users to login directly with their credentials for you can get access to their account and routing number. Stripe has a direct partnership with Plaid so you never come into contact with their banking information and you just pass around tokens to connect their bank to Stripe. This is great for security since you ever have to worry about leaking their bank credentials. Plaid is a great solution if you are accepting larger sized payments and want the users to use ACH bank transfers in Stripe for lower fees.
- **[Baremetrics](https://baremetrics.com/)** - Baremetrics is not a payment processor but it is a great complimentary product to add to your payments stack one you are processing a lot of money. They add great charting and insights and integrate directly into your payment processor.

### Email
WIP...

### Customer service
WIP...

### Terms of Service and Privacy Policy
WIP...

## Contributing
If you would like to contribute please do! The more input we get the better this guide will become. In the coming weeks I will create an official contributing guide but for now here are the steps:

We use [Github Flow](https://guides.github.com/introduction/flow/index.html), so all code changes happen through pull requests. Pull requests are the best way to propose changes to the codebase (we use [Github Flow](https://guides.github.com/introduction/flow/index.html)). We actively welcome your pull requests:

1. Fork the repo and create your branch from `master`.
2. If you've added code that should be tested, add tests.
3. If you've changed APIs, update the documentation.
4. Ensure the test suite passes.
5. Make sure your code lints.
6. Issue that pull request!

## License
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
