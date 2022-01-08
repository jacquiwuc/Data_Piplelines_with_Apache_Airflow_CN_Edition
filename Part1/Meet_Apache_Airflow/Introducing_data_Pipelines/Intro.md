Data pipelines generally consist of several tasks or actions that need to be executed to achieve the desired result. For example, say we want to build a small weather dashboard that tells us what the weather will be like in the coming week (figure 1.1). To implement this live weather dashboard, we need to perform something like the following steps:

1. Fetch weather forecast data from a weather API.
2. Clean or otherwise transform the fetched data (e.g., converting temperatures from Fahrenheit to Celsius or vice versa), so that the data suits our purpose.
3. Push the transformed data to the weather dashboard.

![image](https://github.com/jacquiwuc/Data_Piplelines_with_Apache_Airflow_CN_Edition/blob/main/Part1/Meet_Apache_Airflow/Introducing_data_Pipelines/1.1.png)

As you can see, this relatively simple pipeline already consists of three different tasks that each perform part of the work. Moreover, these tasks need to be executed in a specific order, as it (for example) doesn’t make sense to try transforming the data before fetching it. Similarly, we can’t push any new data to the dashboard until it has undergone the required transformations. As such, we need to make sure that this implicit task order is also enforced when running this data process.



Translation:

数据管道通常是由几个任务构成，用于达到想要的结果。举个例子，如果我们想要做一个图表用于预测下周的天气，为了完成这个，我们得需要实施以下步骤：

1. 从一个天气API萃取天气预测结果；
2. 清理或者转换数据，像是从华氏摄氏度转换成摄氏摄氏度
3. 把转换后的数据嵌入到天气报表里


![image](https://github.com/jacquiwuc/Data_Piplelines_with_Apache_Airflow_CN_Edition/blob/main/Part1/Meet_Apache_Airflow/Introducing_data_Pipelines/1.1.png)

如你所见，这个简单的数据管道已经包括了三个不同的任务。而且，这些任务要以不同的顺序执行，像是不可能在萃取数据前转换数据一样。同样的，也不可能在没清理数据前已经把数据嵌入到图表里。所以，我们需要明确好执行顺序。
