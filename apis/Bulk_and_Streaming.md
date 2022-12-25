# Batch Apex ⏳️

Batch Apex is used to run **large jobs** that would exceed normal processing limits. You can process records asynchronously in batches. 



If you have a lot of records to process, for example, *data cleansing* or *archiving*, Batch Apex is probably your best solution.



## Batch Apex works under the hood

Let’s say you want to process 1 million records using Batch Apex. **The execution logic of the batch class is called once for each batch** of records you are processing.



Each time you invoke a batch class, **the job is placed on the Apex job queue** and is executed as a discrete transaction. This functionality has two awesome advantages:

- *Every transaction starts with a new set of governor limits*, making it easier to ensure that your code stays within the governor execution limits.
- If one batch fails to process successfully, all other *successful batch transactions aren’t rolled back*.



Here’s what the skeleton of a Batch Apex class looks like:


```
🔗public class MyBatchClass implements Database.Batchable<sObject> {

    public (Database.QueryLocator | Iterable<sObject>) start(Database.BatchableContext bc)     {
    // collect the batches of records or objects to be passed to execute
    }
    
    public void execute(Database.BatchableContext bc, List<P> records){
        // process each batch of records
    }
    
    public void finish(Database.BatchableContext bc){
        // execute any post-processing operations
    }
}

```

### [*Check examples and testing in here* 🔗](https://trailhead.salesforce.com/content/learn/modules/asynchronous_apex/async_apex_batch?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-platform-developer-ii-credential)



------



## Best Practices

To ensure fast execution of batch jobs, minimize Web service callout times and tune queries used in your batch Apex code. The longer the batch job executes, the more likely other queued jobs are delayed when many jobs are in the queue.

Best practices include:

- Only use Batch Apex if **you have more than one batch of records**. If you don't have enough records to run more than one batch, you are probably better off using Queueable Apex.
- **Tune any SOQL query** to gather the records to execute as quickly as possible.
- **Minimize the number of asynchronous requests** created to minimize the chance of delays.
- **Use extreme care if you are planning to invoke a batch job from a trigger**. You must be able to guarantee that the trigger won’t add more batch jobs than the limit.

