---
title: "Basic Lambda creation"
metaTitle: "Basic Lambda creation"
metaDescription: "Basic Lambda creation"
---

## Creating
**From The AWS console:**

1. Search for Lambda.
2. Click on **Create Function**.
3. Select a template.
4. Enter a function name.
5. Choose a runtime for your code.
6. In Permissions.
   * Anytime a Lambda function runs, it assumes an execution role to determine its access permission (What can it do, what does it have access to).
7. Create a new role with basic Lambda permissions (gives the function acess to AWS CloudWatch logs).
8. Advanced Settings: Nothing to do here.
9. Click on **Create function**.


## Testing
**From the function dashboard**

1. Enter your code in the file found in the /'your-function-name' dir.
2. Deploy your code by clicking on the **deploy** button.
3. Testing our function.
   * Click on the arrow next to the **Test** button.
   * Configure test event.
   * Give the test a name.
   * Here you can enter the params that will be received by your function when that test event is triggered.
   * Click on **Test** to run it.

## Checking our logs

1. Click on the **monitor** tab.
2. Click on **View logs in CloudWatch**.
3. The **Log streams** column shows the logs across multiple executions of our function.
   1. Click on a log stream.
   2. It shows when the request started, ended, the duration and the build duration, as well as the output.

