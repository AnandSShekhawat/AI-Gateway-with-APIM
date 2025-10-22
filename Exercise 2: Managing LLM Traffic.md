# Exercise 2: Managing LLM Traffic

## Lab Overview

Learn to monitor and control LLM usage through token metrics and rate limiting to optimize costs and performance.


## Task 1: Capture token usage metrics from AI Gateway traffic. 

1. Navigate to **0️⃣ Initialize notebook variables** cell and click on **Run**. Prepare the environment, define resources, models, and subscriptions so everything is ready for deployment.

   ![](./media/API-gateway-image23.png)
   ![](./media/API-gateway-image24.png)

2. Next go to **1️⃣ Verify the Azure CLI and the connected Azure subscription**. This ensure the commands will run in the correct Azure subscription and that we have permissions to create resources.

   ![](./media/API-gateway-image26.png)
   
3. Next **2️⃣ Create deployment using 🦾 Bicep*** click on Run. This cell Automate the creation of APIM, AI Foundry endpoints, and model deployments so that the environment is consistent and reproducible.

   ![](./media/API-gateway-image27.png)

4. Next **3️⃣ Get the deployment outputs**. This rRetrieve URLs, keys, and Application Insights names that are needed to interact with the deployed AI endpoints.

   ![](./media/API-gateway-image28.png)
   
5. Next **🧪 Test the API using a direct HTTP call**. Simulate real API requests to ensure that the token metrics are emitted correctly and that the agent responds as expected.

   ![](./media/API-gateway-image29.png)

   ![](./media/API-gateway-image30.png)

6. Next **🧪 Execute multiple runs for each subscription using the Azure OpenAI Python SDK**. Verify that metrics are tracked consistently across multiple subscriptions and API keys using the official Azure OpenAI SDK.

   ![](./media/API-gateway-image31.png)

7. Next **🔍 Analyze Application Insights custom metrics with a KQL query**, this Query and extract token usage data to monitor consumption and identify patterns.

    ![](./media/API-gateway-image32.png)

8. Next **🔍 Plot the custom metrics results**, this Visualize token usage over time to see trends, spikes, or anomalies.

    ![](./media/API-gateway-image33.png)

9. Next 🔍 See the metrics on the Azure Portal. Validate the token consumption visually for each subscription in Application Insights for easier monitoring.
    
    ![](./media/API-gateway-image34.png)
  
10. Open the Application Insights resource, navigate to the Metrics blade, then select the defined namespace (openai). Choose the metric "Total Tokens" with a Sum aggregation. Then, apply splitting by 'Subscription Id' to view values for each dimension.












https://github.com/Azure-Samples/AI-Gateway/blob/main/labs/token-metrics-emitting/token-metrics-emitting.ipynb



## Task 2: Apply rate limiting policies to control token consumption. 

https://github.com/Azure-Samples/AI-Gateway/blob/main/labs/token-rate-limiting/README.MD
