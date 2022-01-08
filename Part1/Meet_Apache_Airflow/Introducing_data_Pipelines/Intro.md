Data pipelines generally consist of several tasks or actions that need to be executed to achieve the desired result. For example, say we want to build a small weather dashboard that tells us what the weather will be like in the coming week (figure 1.1). To
implement this live weather dashboard, we need to perform something like the following steps:

1. Fetch weather forecast data from a weather API.
2. Clean or otherwise transform the fetched data (e.g., converting temperatures
from Fahrenheit to Celsius or vice versa), so that the data suits our purpose.
3. Push the transformed data to the weather dashboard.

As you can see, this relatively simple pipeline already consists of three different tasks that each perform part of the work. Moreover, these tasks need to be executed in a specific order, as it (for example) doesn’t make sense to try transforming the data before fetching it. Similarly, we can’t push any new data to the dashboard until it has undergone the required transformations. As such, we need to make sure that this implicit task order is also enforced when running this data process.



Translation:
数据管道通常是由几个任务构成，用于达到想要的结果。
