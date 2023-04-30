# New payment gateway integration

At VTEX, you can use the **Payment Provider Protocol** to integrate your payment connector into our platform.

## Prerequisites

Before you implement the integration, you must assure that the following items were covered:
- The business partnership agreement for financial services was signed.
- You have access to a VTEX environment.
- You meet the payment methods requirements

> For more information about the prerequisites, refer to the [Implementation prerequisites](https://help.vtex.com/en/tutorial/payment-provider-protocol--RdsT2spdq80MMwwOeEq0m#implementation-prerequisites) in our Tutorial & Solutions documentation.


## Integrate your payment gateway
To integrate your gateway, you must follow these steps:

#### 1. Implement the protocol 
The first step is to implement the back-end service that will receive and process the payments. For more information, refer to our [Payment protocol flow](https://help.vtex.com/en/tutorial/payment-provider-protocol#payment-protocol-flow) documentation.

#### 2. Identify your specific use case
- If you want to implement the connector through VTEX IO from a boilerplate, which already comes with most of the work done, including the protocol endpoints, follow the [Payment Provider Framework (PPF)](https://developers.vtex.com/vtex-rest-api/docs/payments-integration-payment-provider-framework).
- If you want to implement the PPP application for payments in physical stores using a POS, follow the [Payment Provider Protocol for POS payments](https://developers.vtex.com/vtex-rest-api/docs/payments-integration-ppp-applied-to-pos). 

Afterward, you will receive the access data and deploy the backend.

#### 3. Teste the payment provider
- Install the Payment Provider Test Suite from the [VTEX App Store](https://apps.vtex.com/vtex-payment-provider-test-suite/p).
- In the tool, select **Other module** from the Admin's left-side menu. 
- Select the Payment Provider option to configure it correctly according to the documentation [here](https://help.vtex.com/en/tutorial/payment-provider-protocol--RdsT2spdq80MMwwOeEq0m#service-information).
- Perform the homologation test, as documented [here](https://help.vtex.com/en/tutorial/payment-provider-protocol--RdsT2spdq80MMwwOeEq0m#tests) and [here](https://help.vtex.com/en/tutorial/payment-provider-protocol--RdsT2spdq80MMwwOeEq0m#4-testing).
- Check the results with the help of the documentation [here](https://help.vtex.com/en/tutorial/payment-provider-protocol--RdsT2spdq80MMwwOeEq0m#5-results).

#### 4. Homologation
After the tests are done, open a ticket to our [VTEX support](https://help.vtex.com/en/support) and include the following information:h
- Connector Name
- Partner contact
- Production Service Provider Endpoint
- Sandbox Service Provider Endpoint
- Owner account
- Allowed Accounts
- New Payment methods
- New Payment method purchase flow
